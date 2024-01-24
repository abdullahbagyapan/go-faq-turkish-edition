# Bu projenin amacı nedir ?

<p>Go'nun ortaya çıktığı dönemde, programlama dünyası bugünden farklıydı.
Yazılımlar genellikle C++ veya Java ile yazılırdı, GitHub yoktu, çoğu bilgisayar çok işlemcili değildi, ve Visual Studio ve Eclipse dışında çok az IDE vardı veya diğer üst düzey araçlar çok az sayıda idi.
</p>

<p>
Zamanla, sunucu yazılımı geliştirmek için çalıştığımız dillerin aşırı karmaşıklığı yüzünden hüsrana uğradık.
Bilgisayarlar C, C++ ve Java'nın ilk çıkışından beri son derece hızlanmıştı ancak, programlama onlar kadar ilerleyemedi.
Ayrıca, çoklu işlemcilerin evrensel olmaya başlaması açıkca belliydi ama çoğu dil bunları etkili ve güvenli şekilde programlamak için çok az yardım sağladı.
</p>

<p>
Geri adım atmaya karar verdik ve yıllar ilerledikçe, büyük sorunların yazılım mühendisliğini ele geçireceğini ve yeni bir dilin onlara nasıl yardım edeceğini düşünmeye başladık.
Örneğin, çok çekirdekli işlemcilerin yükselişiyle, bir dilin concurrency ve parallelizm için 1.derece desteğinin olması savunuldu.
Ve büyük bir concurrency programda kaynak yönetimini takip edilebilir hale getirmek için, garbage collection veya en azından güvenli, otomatik, hafıza yönetimi gerekiyordu.
</p>

<p>
Bu düşünceler Go'nun ortaya çıktığı bir dizi tartışmaya yol açtı, önce bir dizi fikir ve istek olarak, sonra bir dil olarak.
Nihai hedef, Go'nun araçları etkinleştirme, kod biçimlendirme gibi sıradan görevleri otomatikleştirme ve büyük kod tabanları üzerinde çalışmanın önündeki engelleri kaldırma
yoluyla, programcıya daha fazla yardımcı olmak için daha fazlasını yapmasıydı.
</p>

Go'nun hedeflerine ve bu hedeflere nasıl ulaşıldığına veya en azından bu hedeflere nasıl yaklaşıldığına ilişkin çok daha kapsamlı bir açıklama makalede mevcuttur. [Go at Google: Language Design in the Service of Software Engineering](https://go.dev/talks/2012/splash.article)