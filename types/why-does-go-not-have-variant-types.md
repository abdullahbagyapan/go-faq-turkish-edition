# Neden Go'da *variant* türler yok ?

Cebirsel türler olarak da bilinen variant türler, bir değerin diğer türlerden birini alabileceğini belirtmenin bir yolunu sağlar. Sistem programlamadaki yaygın bir örnek olarak, bir hata örneğin bir ağ hatası, bir güvenlik hatası veya bir uygulama hatası olduğunu belirtir ve kullanıcının hatanın türünü inceleyerek sorunun kaynağını ayırt etmesine olanak tanır. Başka bir örnek ise, her düğümün farklı türde olabildiği bir sözdizimi ağacıdır: tanımlama, ifade, atama vb.

Go'ya variant türleri eklemeyi düşündük, ancak tartıştıktan sonra interfacelerle kafa karıştırıcı şekilde örtüştükleri için bunları dışarıda bırakmaya karar verdik. Bir değişkenin türü, variant türünün kendisi interfacei olsaydı ne olurdu?

Ayrıca, bazı variant türlerinin adresi zaten dilin kapsamında. Hata örneğini, hatayı tutmak için bir interface değeri ve durumları ayırt etmek için bir tür anahtarı kullanarak ifade etmek kolaydır. Sözdizimi ağacı örneği de o kadar zarif olmasa da yapılabilir.