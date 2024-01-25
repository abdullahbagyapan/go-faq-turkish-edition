# Go yayınlandığında neden generic tipler eklenmedi ?

Go, zaman içinde bakımı kolay olacak sunucu programları yazmak için bir dil olarak tasarlandı. (ayrıntılar için [buraya](https://go.dev/talks/2012/splash.article) bakınız.)
Go'nun tasarımında ölçeklenebilirlik, okunabilirlik ve concurrency gibi konulara odaklanıldı.
Polymorphic programlama o zamanlar dilin hedefleri açısından gerekli görünmüyordu ve bu nedenle başlangıçta basitlik nedeniyle dışarıda bırakıldı.

<br>

Generic yapılar kullanışlıdır ama type sistemi ve runtime üzerindeki karmaşıklık açısından bir maliyete sahiptirler.
Karmaşıklıkla orantılı değer verdiğine inandığımız bir tasarımı geliştirmek biraz zaman aldı.