# Neden tür kalıtımı yok ?

Nesne yönelimli programlama - en azından en iyi bilinen dillerde - türler arasındaki ilişkilerin, genellikle otomatik olarak türetilen ilişkilerin çok fazla tartışılmasını içerir.
Go farklı bir yaklaşım benimsiyor.

<br>

Programcının önceden iki türün ilişkili olduğunu beyan etmesini gerektirmek yerine, Go'da bir tür, methodlarının bir alt kümesini belirten herhangi bir interfacei otomatik olarak karşılar.
Not tutmayı azaltmanın yanı sıra bu yaklaşımın gerçek avantajları da var.
Türler, geleneksel çoklu kalıtımın karmaşıklığı olmadan birçok interfacei aynı anda karşılayabilir.
Interfaceler, orijinal türlere açıklama eklenmeden çok hafif olabilir.
Türler ve interfaceler arasında açık bir ilişki olmadığından yönetilecek veya tartışılacak bir tür hiyerarşisi yoktur.

<br>

Bu fikirleri, type-safe Unix pipe'larına benzer bir şey oluşturmak için kullanmak mümkündür.
Örneğin, *fmt.Fprintf*'in yalnızca bir dosyaya değil, herhangi bir çıktıya biçimlendirilmiş yazdırmayı nasıl mümkün kıldığını veya *bufio* paketinin dosya I/O'sundan nasıl tamamen ayrı olabileceğini veya *image* paketlerinin nasıl sıkıştırılmış görüntü dosyaları oluşturduğuna bakın.
Tüm bu fikirler, tek bir interface'in(io.Writer), tek bir methodundan(Write) kaynaklanmaktadır.
Ve bu sadece yüzeyi şekillendiriyor. Go'nun interfacelerinin programları nasıl yapılandırıldığı üzerinde derin bir etkisi vardır.

<br>

Alışmak biraz zaman alır ancak tür bağımlılığının bu örtülü tarzı Go'nun en üretken yanlarından biridir.