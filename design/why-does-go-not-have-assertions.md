# Neden Go'da *assertion*'lar yok ?

Assertionlar inkar edilemez derecede kullanışlılar, ama Go'da yoklar.
Deneyimlerimiz, programcıların bunları doğru hata yönetimi ve raporlamadan kaçınmak için bir koltuk değneği olarak kullandıkları yönündedir.
Doğru hata yönetimi, sunucuların ölümcül olmayan bir hatadan sonra çökmek yerine çalışmaya devam etmesi anlamına gelir.
Doğru hata raporlaması, hataların doğrudan ve hedefe yönelik olduğu anlamına gelir ve programcıyı hatanın izini sürmekten kurtarır.
Hataları gören programcının koda aşina olmadığı durumlarda ölümcül hatalar özellikle önemlidir.

<br>

Bunun bir tartışma noktası olduğunu anlıyoruz.
Go dilinde ve kütüphanelerinde modern uygulamalardan farklı olan pek çok şey var, çünkü bazen farklı bir yaklaşımın denemeye değer olduğunu düşünüyoruz.