# Neden *thread*'ler yerine *goroutine*'ler ?

Goroutineler, concurrency kullanımını kolaylaştırmanın bir yoludur.
Bir süredir ortalıkta dolaşan fikir, bağımsız olarak çalıştırılan fonksiyonları (coroutineler) bir dizi thread üzerinde çoğaltmaktır.
Bir coroutine, örneğin bir sistem çağrısını çağırarak bloke olduğunda, run-time otomatik olarak aynı işletim sistemindeki thread üzerinde olan diğer coroutineleri farklı bir threade taşır, böylece bloklanamazlar.
Programcı yapılanların hiçbirini görmüyor, asıl mesele de bu.
Sonuç olarak, Goroutineler çok ucuz olabilir: hafıza için yalnızca birkaç kilobaytlık bellek maliyetinin ötesinde çok az yükleri vardır.

<br>

Hafızadaki yığınları küçültmek için Go run-time'ı yeniden boyutlandırılabilir ve sınırlı sayıda yığın kullanır.
Yeni oluşturulmuş bir goroutine yalnızca birkaç kilobayt boyutundadır ve bu neredeyse her zaman yeterlidir.
Yeterli olmadığı durumlarda ise, run-time, yığının depolanması için belleği otomatik olarak büyütür/küçültür böylece birçok goroutine mütevazı bir bellek miktarında yaşamasına olanak tanır.
CPU yükünün ortalaması, fonksiyon çağrısı başına yaklaşık 3 tane basit/ucuz işlemdir.
Aynı adres uzayında yüzbinlerce goroutine oluşturmak pratiktir.
Goroutineler yalnızca thread olsaydı, sistem kaynakları hemen tükenirdi.