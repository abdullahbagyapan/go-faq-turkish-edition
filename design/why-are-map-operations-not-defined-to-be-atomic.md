# Neden *map* işlemleri *atomic* değil ?

Uzun tartışmalardan sonra, map yapısının normal kullanımının birden fazla goroutine tarafından güvenli erişim gerektirmediğine karar verildi.
Gerektiği durumlarda ise map yapısı muhtemelen daha büyük bir veri yapısının veya halihazırda senkronize edilmiş bir hesaplamanın parçasıydı.
Bu nedenle, tüm map işlemlerinin bir mutex kullanması çoğu programı yavaşlatacak ve sadece birkaç programa güvenlik katacaktır.
Ancak bu kolay bir karar değildi çünkü kontrolsüz map erişiminin programın çökmesine neden olabileceği anlamına geliyordu.

<br>

Dil, map üzerinde senkron veri güncellemelerini engellemez. Gerektiğinde, örneğin güvenilmeyen bir programı çalıştırırken, uygulama map erişimini kilitleyebilir.

<br>

Map erişimi yalnızca veri üzerinde güncellemeler gerçekleştiğinde güvenli değildir.
Tüm goroutineler yalnızca map değerlerini okuduğu(map üzerinde değer aramak, for range döngüsü ile değerleri gezmek) ve değerler üzerinde oynama(atama - silme işlemleri) yapmadığı sürece, map üzerinde senkronizasyon olmadan aynı anda erişmeleri güvenlidir.

<br>

Map kullanımını düzeltmeye yardımcı olarak, dilin içindeki bazı uygulamalar, çalışma zamanında bir map eş zamanlı olarak güvenli olmayan bir şekilde değiştirildiğinde otomatik olarak rapor veren özel bir kontrol içerir.