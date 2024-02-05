# Neden Go'da *covariant result* türleri yok ?

Kovaryant result türleri, şöyle bir arayüzün olduğu anlamına gelir:

```go
type Copyable interface {
    Copy() interface{}
}
```

şöyle bir method ile implemente eder,

```go
func (v Value) Copy() Value
```

çünkü *Value* boş bir interfacei implemente ediyor. Go'da method türlerinin tam olarak eşleşmesi gerekir, bu nedenle *Value*, *Copyable*'i implemente edemez. Go, bir türün ne yaptığı kavramını (methodlarını) türün implemantasyonundan ayırır. Eğer iki method farklı türler döndürüyorsa aynı şeyi yapmıyorlar demektir. Kovaryant result türleri isteyen programcılar genellikle interfaceler aracılığıyla bir tür hiyerarşisini ifade etmeye çalışırlar. Go'da interface ile implemantasyon arasında net bir ayrım olması daha doğaldır.