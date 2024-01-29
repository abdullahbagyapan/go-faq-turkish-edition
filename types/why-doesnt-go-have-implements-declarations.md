# Neden Go'da *implement* tanımı yok ?

Go'da türler, bir interface'i içindeki tanımlı methodlarını uygulayarak implemente ederler, bundan başka bir şey değil.
Bu özellik, interfacelerin mevcut kodu değiştirmeye gerek kalmadan tanımlanmasına ve kullanılmasına olanak tanır.
[Farklı bölümlere](https://en.wikipedia.org/wiki/Separation_of_concerns) ayrılmasını teşvik eden ve kodun yeniden kullanımını geliştiren bir tür [yapısal yazım](https://en.wikipedia.org/wiki/Structural_type_system) kolaylığı sağlar, ve kod geliştikçe ortaya çıkan kalıplardan yararlanmayı kolaylaştırır.
Interfacelerin anlamı, Go'nun çevik ve hafif hissinin ana nedenlerinden biridir.

<br>

Daha ayrıntılı bilgi için [tür mirası](/types/why-is-there-no-type-inheritance.md) hakkındaki soruya bakın.