# Go'nun tasarımındaki yol göstericiler nelerdir ?

Go tasarlandığında, Java ve C++ Google'da sunucu yazmak için en çok kullanılan dillerdi.
Bu dillerin çok fazla not alma ve tekrar gerektirdiğini hissettik.
Bazı programcılar, verimlilik ve tür güvenliği pahasına Python gibi daha dinamik, akıcı dillere yönelerek tepki gösterdi.
Verimliliği, güvenliği ve akıcılığı tek bir dilde elde etmenin gerekliliğini hissettik.

<br>

Go, kelimenin her anlamında yazma miktarını azaltmaya çalışıyor.
Tasarımı boyunca dağınıklığı ve karmaşıklığı azaltmaya çalıştık.
Herhangi bir ön tanımlama veya header dosyayı yok; herşey sadece 1 kere tanımlanır.
Tanımlama yapmak etkileyici, otomatik ve kullanımı kolaydır.
Syntax'i temiz ve keywordler açısından hafiftir.
Tekrarlar (`foo.Foo* myFoo = new(foo.Foo)`), `:=` kullanarak azaltılmıştır. (`myFoo := new(foo.Foo)`)
Ve belki de en radikali, tür hiyerarşisinin olmamasıdır.
Türler sadece olduğu gibiler, İlişkilerini duyurmak zorunda değiller.
Bu basitleştirmeler, Go'nun hem etkileyici hem de anlaşılır olmasını sağlar.

<br>

Bir diğer önemli prensip ise kavramları açık tutmaktır.
Methodlar, herhangi bir type için implemente edilebilir.
Açıklık, herşey birleştiğinde ne olacağını anlamayı kolaylaştırır.