# Neden Go'da *exception*'lar yok ?

Try-catch-finally yapısında olduğu gibi exceptionların bir kontrol yapısına bağlanmasının karmaşık kodla sonuçlanacağına inanıyoruz.
Ayrıca programcıları, bir dosyayı açamamak gibi çok sayıda sıradan hatayı, olağan olarak etiketlemeye teşvik etme eğilimindedir.

<br>

Go farklı bir yaklaşım benimsiyor.
Düz hata yönetimi için Go'nun birden fazla return değerleri, hatayı bildirmeyi kolaylaştırır.
[Error type](https://go.dev/blog/error-handling-and-go), Go'nun diğer özellikleriyle birleştiğinde hata işlemeyi keyifli hale getirir ancak diğer dillerden oldukça farklıdır.

<br>

Go ayrıca gerçekten olağanüstü durumlarda sinyal vermek ve bu durumlardan kurtulmak için birkaç yerleşik işleve sahiptir.
Kurtarma mekanizması yalnızca bir fonksiyonun hatadan sonra bir parçası olarak yürütülür; bu felaketle başa çıkmak için yeterlidir ve güzel kullanıldığında temiz kod ile sonuçlanabilir.

<br>

Ayrıntılar için [Defer, Panic ve Recover](https://go.dev/blog/defer-panic-and-recover) makalelerine bakın.
Ayrıca, [Errors are values](https://go.dev/blog/errors-are-values) gönderisi, Go'da hataların temiz bir şekilde ele alınmasına yönelik bir yaklaşımı açıklar.
Hatalar yalnızca bir değer olduğundan, Go'nun tüm gücünün hata işlemede kullanılabileceğini göstermektedir.