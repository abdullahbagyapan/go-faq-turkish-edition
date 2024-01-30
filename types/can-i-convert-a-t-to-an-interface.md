# []T'yi []interface'e çevirebilir miyim ?

Direkt olarak değil.
Dil yazımı buna izin vermiyor çünkü iki tür bellekte aynı şekilde temsil edilmiyor.
Her bir elemanı tek tek hedef *slice*'a kopyalamak gerekir.
Bu örnek, bir grup *int*'i, bir grup interface'e dönüştürüyor:

```go
t := []int{1, 2, 3, 4}
s := make([]interface{}, len(t))
for i, v := range t {
    s[i] = v
}
```