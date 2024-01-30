# Eğer []1 ve []2 aynı type'dan geliyorsa, birbirlerine dönüştürebilir miyim ?

Bu kod örneğinin son satırı derlenmiyor:

```go
type T1 int
type T2 int

var t1 T1
var x = T2(t1) // OK

var st1 []T1
var sx = ([]T2)(st1) // NOT OK
```

Go'da türler methodlara yakından bağlıdır; her adlandırılmış türün (muhtemelen boş) bir yöntem kümesi vardır.
Genel kural, dönüştürülen türün adını değiştirebilmenizdir(muhtemelen yöntem setide değişiyor) ancak bileşik türdeki öğelerin adını (ve yöntem kümesini) değiştiremezsiniz.
Go'da tür dönüşümleri konusunda açık olmanız gerekir.