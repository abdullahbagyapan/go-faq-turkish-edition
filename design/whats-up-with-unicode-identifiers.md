# Unicode tanımlayıcılarından ne haber ?

Go'yu tasarlarken aşırı ASCII merkezli olmadığından emin olmak istedik.
Bu, tanımlayıcıların alanını, 7 bitlik ASCII'yle sınırlamamak anlamına geliyordu.
Go'nun kuralının anlaşılması ve uygulanması basittir ancak kısıtlamaları vardır, Örneğin karakterlerin birleştirilmesi -*Devanagari* gibi bazı diller hariç- tasarım nedeniyle eklenmemiştir.

<br>

Bu kuralın başka bir talihsiz sonucu daha var.
Dışa aktarılan bir tanımlayıcının büyük harfle başlaması gerektiğinden, bazı dillerdeki karakterlerden oluşturulan tanımlayıcılar tanım gereği dışa aktarılamaz.
ya da şimdilik tek çözüm, açıkça tatmin edici olmayan *X日本語* gibi bir şey kullanmaktır.

<br>

Dilin en eski versiyonundan bu yana, diğer ana dilleri kullanan programcılara uyum sağlamak için tanımlayıcı alanın en iyi şekilde nasıl genişletilebileceği konusunda önemli düşünceler olmuştur.
Tam olarak ne yapılacağı aktif bir tartışma konusu olmaya devam ediyor ve dilin gelecekteki bir versiyonu, tanımlayıcı tanımı açısından daha liberal olabilir.
Örneğin, Unicode kuruluşunun tanımlayıcılara yönelik [tavsiyelerindeki](https://unicode.org/reports/tr31/) bazı fikirleri benimseyebilir.
Ne olursa olsun, Go'nun en sevdiğimiz özelliklerinden biri olmaya devam eden tanımlayıcıların görünürlüğünü belirleyen harf büyüklüğünün korunma biçimi (veya belkide genişletme) uyumlu bir şekilde yapılmalıdır.

<br>

Şimdilik, programları bozmadan daha sonra genişletilebilecek basit bir kuralımız var, belirsiz tanımlayıcıları kabul eden bir kuraldan kaynaklanacağı kesin olan hataları önleyen bir yöntem.