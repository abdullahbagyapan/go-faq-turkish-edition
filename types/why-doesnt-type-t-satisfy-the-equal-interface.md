# Neden *T* type'ı *interface*'e eşit değil ?

Kendisini başka bir değerle karşılaştırabilen bir nesneyi temsil eden bu basit interface'i düşünün:

```go
type Equaler interface {
    Equal(Equaler) bool
}
```

ve bu da type T:

```go
type T int
func (t T) Equal(u T) bool { return t == u } // Equaler interface'ini karşılamıyor
```

Bazı polimorfik tip sistemlerdeki benzer durumun aksine, T *Equaler*'ı implemente etmiyor.
T.Equal()'in parametre türü T'dir, gerekli olan Equaler değildir.

<br>

Go'da tür sistemi *Equal* argümanını desteklemez; -Equaler'ı uygulayan T2 türünde gösterildiği gibi- bu, programcının sorumluluğundadır:

```go
type T2 int
func (t T2) Equal(u Equaler) bool { return t == u.(T2) }  // Equaler interface'ini karşılar
```

Ancak bu bile diğer tür sistemlerine benzemez, çünkü Go'da Equaler'ı karşılayan *herhangi* bir tür T2.Equal'e parametre olarak iletilebilir ve çalışma zamanında parametrenin T2 türünde olup olmadığını kontrol etmeliyiz.
Bazı diller bu garantiyi derleme zamanında sağlar.

<br>

Başka bir ilgili örnek:

```go
type Opener interface {
   Open() Reader
}

func (t T3) Open() *os.File
```

Go'da T3, başka bir dilde olsa da Opener'ı karşılamıyor.

<br>

Bu gibi durumlarda Go'nun tür sisteminin programcıya daha az şey yaptığı doğru olsa da, alt tür olmayışı interface karşılamasına ilişkin kuralların belirtilmesini çok kolaylaştırıyor.
Fonksiyonun adları ve imzaları tam olarak interface'in adları ve imzaları mı?
Go'da kuralların verimli bir şekilde uygulanması da kolaydır.
Bu avantajların, otomatik tür tanıtımının eksikliğini telafi ettiğini düşünüyoruz.
Go'nun bir gün, bir tür polimorfik yazım biçimini benimsemesi durumunda, bu örnekleri ifade etmenin ve ayrıca bunların statik olarak kontrol edilmesini sağlamanın bir yolu olacağını umuyoruz.