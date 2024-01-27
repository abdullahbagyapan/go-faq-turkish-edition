# Değiştirdiğim özellikleri kabul edecek misiniz ?

İnsanlar sıklıkla dilde iyileştirmeler öneriyor - [posta listesi](https://groups.google.com/group/golang-nuts) bu tür tartışmaların zengin bir geçmişini içeriyor - ancak bu değişikliklerin çok azı kabul edildi.

<br>

Go açık kaynaklı bir proje olmasına rağmen dil ve kütüphaneler, mevcut programları en azından kaynak kodu düzeyinde bozan değişiklikleri önleyen bir [uyumluluk vaadiyle](https://go.dev/doc/go1compat) korunmaktadır (programların güncel kalması için ara sıra yeniden derlenmesi gerekebilir).
Teklifiniz Go 1 spesifikasyonunu ihlal ediyorsa, değeri ne olursa olsun bu fikri dikkate bile alamayız.
Go'nun gelecekteki büyük bir sürümü Go 1 ile uyumsuz olabilir, ancak bu konudaki tartışmalar daha yeni başladı ve kesin olan bir şey var: süreçte bu tür uyumsuzlukların çok az olacağıdır.
Üstelik uyumluluk vaadi, böyle bir durumun ortaya çıkması durumunda eski programların uyum sağlaması için ileriye doğru bir yol sağlama konusunda bizi teşvik etmektedir.

<br>

Teklifiniz Go 1 spesifikasyonuyla uyumlu olsa bile Go'nun tasarım hedeflerine uygun olmayabilir.
[Go at Google: Language Design in the Service of Software Engineering](https://go.dev/talks/2012/splash.article) Go'nun kökenlerini ve tasarımının ardındaki motivasyonu açıklıyor.