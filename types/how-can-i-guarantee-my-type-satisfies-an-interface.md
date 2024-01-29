# Nasıl type'ın *interface*'i implemente ettiğini bilirim ?

T türü için boş bir değeri veya T pointerını kullanarak bir atama işlemini yaparak, T türünün I interface'ini implemente edip etmediği derleyiciden öğrenebilirsiniz.

```go
type T struct{}
var _ I = T{}       // T'nin I'yı implemente ettiğini doğrular
var _ I = (*T)(nil) // *T'nin I'yı implemente ettiğini doğrular
```

Eğer T (veya *T) I'yi implemente etmezse, hata derleme zamanında yakalanacaktır.

<br>

Bir interface'in kullanıcılarının onu implemente ettiklerini açıkça beyan etmelerini istiyorsanız, interface'deki methodlar setine açıklayıcı bir adla bir method ekleyebilirsiniz.
Örneğin:

```go
type Fooer interface {
    Foo()
    ImplementsFooer()
}
```

Bir türün Fooer olması için *ImplementsFooer* methodunu tanımlamalı, gerçeği açıkça belgelemeli ve bunu [go doc](https://pkg.go.dev/cmd/go#hdr-Show_documentation_for_package_or_symbol)'un çıktısında belirtmelidir.

```go
type Bar struct{}
func (b Bar) ImplementsFooer() {}
func (b Bar) Foo() {}
```

Çoğu kod, interface fikrinin faydalarını sınırladığından bu tür kısıtlamalardan yararlanmaz.
Ancak bazen benzer interfaceler arasındaki belirsizlikleri çözmek için bunlar gerekli olabilir.