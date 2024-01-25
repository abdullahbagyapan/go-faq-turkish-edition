# Go, C/C++ ile beraber çalışabilir mi ?

Aynı adres uzayında C ve Go beraber çalışabilir ancak özel interface yazılımı gerekebilir, ayrıca doğal bir uyum olmayacaktır.
Ayrıca C ve Go'yu birbirine bağlamak, Go'nun sağladığı memory safety ve stack yönetimi özelliklerini devre dışı bırakır.
Bazen bir sorunu çözmek için C kütüphanelerini kullanmak gerekebilir, ancak bunu yapmak her zaman Go kodunda mevcut olmayan bir risk unsuru doğurur; bu nedenle dikkatli olun.

<br>

Go ile C kullanmanız gerekiyorsa nasıl ilerleyeceğiniz Go derleyici uygulamasına bağlıdır.
Go ekibi tarafından desteklenen 3 tane Go derleyicisi vardır.
Bunlar; *gc*, varsayılan derleyici, *gccgo*, gcc temelli, ve yeni olan *gollvm*, LLVM temelli.

<br>

Gc, C'den farklı bir calling convention ve linker kullanır ve bu nedenle doğrudan C programlarından çağrılamaz, veya tamtersi.
[Cgo](https://pkg.go.dev/cmd/cgo) programı, C kütüphanelerini Go koduna güvenli bir şekilde çağrılmasına olanak tanıyan bir "foreign function interface" mekanizması sağlar. Bu yetenek SWIG ile C++ kütüphanelerinide kapsar.

<br>

Cgo ve SWIG'yi gccgo ve gollvm ile de kullanabilirsiniz.
Geleneksel API kullandıkları için, GCC/LLVM ile derlenmiş C veya C++ kodlarını birbirlerine bağlayabilmeniz mümkündür.
Ancak bunu güvenli bir şekilde yapmak, ilgili tüm diller için calling conventionların anlaşılmasının yanı sıra Go'dan C veya C++ çağrılırken stack sınırlarına dikkat edilmesini gerektirir.