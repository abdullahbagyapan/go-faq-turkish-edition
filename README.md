# Go Sık Sorulan Sorular (SSS)

> **Çevirmen Notu**
>
> Bu döküman [Frequently Asked Questions (FAQ)](https://go.dev/doc/faq) adlı yazıdan tercüme edilmiştir.
>
> Yazım veya çeviri yanlışı gördüğünüz yerleri bildirirseniz çok sevinirim.
>
> Son güncelleme tarihi: *30/1/2024*


## İçerik

* Kökenler
    * [Bu projenin amacı nedir ?](origins/what-is-the-purpose-of-the-project.md)
    * [Bu projenin geçmişi nedir ?](origins/what-is-the-history-of-the-project.md)
    * [*Gopher* maskotunun hikayesi nedir ?](origins/what-is-the-origin-of-the-gopher-mascot.md)
    * [*Go* mu yoksa *Golang* mi ?](origins/is-the-language-called-go-or-golang.md)
    * [Neden yeni bir dil yarattınız ?](origins/why-did-you-create-a-new-language.md)
    * [Go nereden esinlenildi ?](origins/what-are-go-ancestors.md)
    * [Go'nun tasarımındaki yol göstericiler nelerdir ?](origins/what-are-the-guiding-principles-in-the-design.md)
* Kullanım
    * [Google kendi içinde Go kullanıyor mu ?](usage/is-google-using-go-internally.md)
    * [Başka hangi şirketler Go'yu kullanıyor ?](usage/what-other-companies-use-go.md)
    * [Go, C/C++ ile beraber çalışabilir mi ?](usage/do-go-programs-link-with-c-cpp-programs.md)
    * [Hangi *IDE*ler Go'yu destekliyor ?](usage/what-ides-does-go-support.md)
    * [Go, Google'ın *protocol buffer*'ını destekliyor mu ?](usage/does-go-support-googles-protocol-buffers.md)
    * [Go'nun anasayfasını başka bir dile tercüme edebilir miyim ?](usage/can-i-translate-the-go-home-page-into-another-language.md)
* Dizayn
    * [Go *runtime*'a sahip mi ?](design/does-go-have-a-runtime.md)
    * [Unicode tanımlayıcılarından ne haber ?](design/whats-up-with-unicode-identifiers.md)
    * [Neden Go *X* özelliğine sahip değil ?](design/why-does-go-not-have-feature-x.md)
    * [Go'ya *generic* yapılar ne eklendi ? ](design/when-did-go-get-generic-types.md)
    * [Go yayınlandığında neden generic tipler eklenmedi ?](design/why-was-go-initially-released-without-generic-types.md)
    * [Neden Go'da *exception*'lar yok ?](design/why-does-go-not-have-exceptions.md)
    * [Neden Go'da *assertion*'lar yok ?](design/why-does-go-not-have-assertions.md)
    * [Neden CSP'ye göre *concurrency* inşa edildi ?](design/why-build-concurrency-on-the-ideas-of-csp.md)
    * [Neden *thread*'ler yerine *goroutine*'ler ?](design/why-goroutines-instead-of-threads.md)
    * [Neden *map* işlemleri *atomic* değil ?](design/why-are-map-operations-not-defined-to-be-atomic.md)
    * [Değiştirdiğim özellikleri kabul edecek misiniz ?](design/will-you-accept-my-language-change.md)
* Türler
    * [Go, *object-oriented* bir dil mi ?](types/is-go-an-object-oriented-language.md)
    * [Methodları nasıl dinamik yaparım ?](types/how-do-i-get-dynamic-dispatch-of-methods.md)
    * [Neden *inheritance* yok ?](types/why-is-there-no-type-inheritance.md)
    * [Neden *len* bir fonksiyon, ve neden bir method değil ?](types/why-is-len-a-function-and-not-a-method.md)
    * [Neden Go, methodlarda ve operatörlerde *overloading*i desteklemiyor ?](types/why-does-go-not-support-overloading-of-methods-and-operators.md)
    * [Neden Go'da *implement* tanımı yok ?](types/why-doesnt-go-have-implements-declarations.md)
    * [Nasıl type'ın *interface*'i implemente ettiğini bilirim ?](types/how-can-i-guarantee-my-type-satisfies-an-interface.md)
    * [Neden *T* type'ı *interface*'e eşit değil ?](types/why-doesnt-type-t-satisfy-the-equal-interface.md)
    * [[]T'yi []interface'e çevirebilir miyim ?](types/can-i-convert-a-t-to-an-interface.md)
    * Eğer []1 ve []2 aynı type'dan geliyorsa, birbirlerine dönüştürebilir miyim ?
    * Neden *nil error*'um *nil*'e eşit değil ?
    * Neden *union*'lar yok, tıpkı *C*'deki gibi ?
    * Neden Go'nun *variant type*'lar yok ?
    * Neden Go'nun *covariant result type*'ları yok ?
* Değerler
    * Neden Go sayılar arası dönüşüm sağlamıyor ?
    * Go'da *constant*'lar nasıl çalışıyor ?
    * Neden *map*'ler *built in* geliyor ?
    * Neden *map*'ler *slice*'ları *key* olarak kabul etmiyor ?
    * Neden *array*'ler değer iken, *map*'ler *slice*'lar ve *channel*'lar referans tipinde ?
* Kod Yazımı
    * Kütüphaneler nasıl belgelendi ?
    * Go programlama stili için bir rehber var mı ?
    * Yamaları nasıl Go kütüphanelerinde paylaşırım ?
    * Neden "*go get*", repository klonlarken HTTPS kullanıyor ?
    * "*go get*" kullanırken paket versiyonlarını nasıl yönetmeliyim ?
* Pointer'lar ve Allocation
    * Ne zaman fonksiyon parametreleri değer olarak geçilmeli ?
    * Ne zaman interface yerine pointer kullanmalıyım ?
    * Değer üzerine veya pointer üzerine method tanımlamalıyım ?
    * *new* ve *make* arasındaki fark nedir ?
    * 64 bit makinede *int*'ın boyutu nedir ?
    * Bir değişkenin *heap*'temi yoksa *stack*'temi tanımlandığını nereden bileceğim ?
    * Neden Go process'ler çok fazla sanal hafıza kullanıyor ?
* Concurrency
    * Hangi işlemler *atomic* ? Peki ya *mutex*'ler ?
    * Programım daha çok cpu ile neden daha hızlı çalışmıyor ?
    * Cpu sayısını nasıl kontrol ederim ?
    * Neden *goroutine*'lerin id'si yok ?
* Fonksiyonlar ve Methodlar
    * Neden T ve *T farklı methodlara sahip ?
    * *Closure*'lar goroutine gibi çalışsa ne olur ?
* Akış Kontrolu
    * Neden Go'da *?:* operatörü yok ?
* Type Parametreleri
    * Neden Go'da type parametreleri var ?
    * *Generic* yapılar Go'ya nasıl eklendi ?
    * Go'daki *generic*'ler ile diğer dillerdeki *generic*'ler arasıdaki farklar ?
    * Neden Go, type parametre listesi için köşeli parantez kullanıyor ?
    * Neden Go, type parametreli methodları desteklemiyor ?
    * Neden parametreli type için daha specific bir type kullanamıyorum ?
    * Neden derleyici, type argumanından anlam çıkarmıyor ?
* Paketler ve Testler
    * Nasul çok dosyalı bir paket oluştururum ?
    * Nasıl *unit test* yazarım ?
    * Test için favori yardımcı fonksiyonum nerede?
    * Neden *X* standart kütüphanede yok ?
* Implementation
    * Derleyiciler için hangi teknolojiler kullanıldı ?
    * *run-time* desteği nasıl eklendi ?
    * Küçük programımın boyutu neden çok fazla ?
    * Kullanılmayan değişken/import'ların uyarısını kapatabilir miyim ?
    * Neden antivirüs programım Go'nun zararlı olduğunu düşünüyor ?
* Performans
    * Neden *X* benchmarkında Go kötü performans gösteriyor ?
* C'den Değişiklikler
    * Neden *syntax* C'den çok farklı ?
    * Neden tanımlamalar geriye doğru yapılıyor ?
    * Neden pointer aritmetiği yok ?
    * Neden *++* ve *--* *statement* neden *expression* değil ? Ve neden *postfix* neden *prefix* değil ?
    * Süslü parantez var ama neden noktalı virgül yok ? Ve neden süslü paraztezi yeni satırdan başlatamıyorum ?
    * *garbage collection* neden yapıldı ? Çok pahalı olmaz mı ?
