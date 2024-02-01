# Neden *nil error*'um *nil*'e eşit değil ?

Interface'ler 2 tane özellik tutarlar, bir tanesi tür(T) diğeri değer(V).
V, somut bir değeri temsil eder, int, struct veya pointer gibi (asla interface'in kendisini tutmaz).
Örneğin, int 3 değerini bir interface'de tutarsak, ortaya çıkan interface şöyle olur: (T:int, V:3).
V değeri, interface'in *dinamik* değeri olarakta bilinir, çünkü program çalıştığı sürece interface'in V değeri değişebilir.

<br>

Bir interface'in değerinin *nil* olması için, ancak ve ancak T ve V değerlerinin atanmamış olmasına bağlıdır (T:nil, V:atanmamış).
Özellikle bir interface nil ise türü kesinlikle nil'dir.
Eğer bir interface'in içinde int tipinde nil pointer saklarsak, ne olursa olsun ortaya çıkan interface şöyle olur: (T:int*, V:nil).
Bu yüzden artık interface'in değeri nil olsa bile kendisi nil olmayacaktır.

<br>

Bu durum kafa karıştırıcı olabilir, bu durumlar interface'in nil değer tuttuğu zaman yaşanır, tıpkı aşağıdaki örnek gibi:

```go
func returnsError() error {
    var p *MyError = nil
    if bad() {
        p = ErrBad
    }
    return p // her zaman non-nil değer dönecek (T:*MyError, V:nil)
}
```

Herşey iyi giderse fonksiyon, nil değer tutan *error* interface'ini dönecektir.
Bunun anlamı, fonksiyonu çağıran kişi, döndürülen hatayı nil ile karşılaştırdığı zaman hata olmasa bile her zaman bir hata varmış gibi görünecektir.
Çağrıyı yapan kişiye bir nil değer döndürmek için, fonksiyon açık bir şekilde nil dönmelidir.

```go
func returnsError() error {
    if bad() {
        return ErrBad
    }
    return nil
}
```

Hata döndüren fonksiyonlarda *'*MyError'* gibi somut değer dönmek yerine her zaman *error* türünü kullanmak hatanın doğru oluşturulduğu garantilemek için daha iyi bir fikirdir.
Örnek olarak os.Open, hata olduğunda her zaman *'*os.PathError'* dönmesine rağmen fonksiyon *error* dönüyor.

<br>

Burada açıklananlara benzer durumlar, interface'ler kullanıldığında ortaya çıkabilir.
Eğer interface'in içinde herhangi bir somut değer saklanıyorsa, interface nil olmayacaktır.
Daha fazla bilgi için [The Laws of Reflection](https://go.dev/blog/laws-of-reflection) makalesini inceleyin.