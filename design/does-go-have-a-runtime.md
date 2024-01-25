# Go *runtime*'a sahip mi ?

Her Go programında var olan, Go'nun *runtime* adında yaygın kullanılan bir kitaplığı var.
Runtime kitaplığı, Go dilinin garbage collection, concurrency, stack management ve diğer kritik özelliklerini implemente eder.
Dil açısından daha merkezi olmasına rağmen Go'nun runtime'ı, C kitaplığı olan *libc*'ye benzer.

<br>

Ancak Go'nun runtimeı, Java runtimeı gibi bir sanal makine içermediğini anlamak önemlidir.
Go programları önceden makine koduna(ahead of time) göre derlenir.
Bu nedenle, terim sıklıkla bir programın çalıştığı sanal ortamı tanımlamak için kullanılsa da, Go'da "runtime" sözcüğü yalnızca kritik dil hizmeti sağlayan kitaplığa verilen addır.