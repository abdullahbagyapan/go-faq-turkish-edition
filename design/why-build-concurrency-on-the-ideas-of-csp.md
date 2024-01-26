# Neden CSP'ye göre *concurrency* inşa edildi ?

Concurrency ve multi-threading programlama, zamanla zorluk üzerine ün kazandı.
Bunu kısmen [pthread](https://en.wikipedia.org/wiki/Pthreads)'ler gibi karmaşık tasarımlardan ve birazda olsa mutexler, koşul değişkenleri ve bellek engelleri gibi low-level ayrıntılara aşırı vurgu yapılmasından kaynaklandığına inanıyoruz.
Daha yüksek seviyeli arayüzler, konunun içinde hala mutexler ve benzeri şeyler olsa bile, çok daha basit kodlara olanak tanır.

<br>

Concurrency için üst düzey dil desteği sağlamaya yönelik en başarılı modellerden biri, Hoare'nin Communicating Sequential Processes(İletişim Sıralı Süreçler) veya CSP'den gelir.
Occam ve Erlang, CSP kökenli, iyi bilinen iki dildir.
Go'nun concurrency temelleri aile ağacının farklı bir bölümünden , birinci sınıf nesne olan *channel*lardan türemiştir.
Daha önceki birkaç dille(*Occam ve Erlang*) ilgili deneyimler, CSP modelinin prosedürel dil çerçevesine iyi uyduğunu göstermiştir.