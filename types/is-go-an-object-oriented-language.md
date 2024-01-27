# Go, *object-oriented* bir dil mi ?

Hem evet hem hayır. Go'da typelar ve methodlar olmasına ve nesne yönelimli programlama stiline izin vermesine rağmen, tür hiyerarşisi yoktur.
Go'daki "interface" kavramı, kullanımının kolay ve bazı açılardan daha genel olduğuna inandığımız farklı bir yaklaşım sunuyor.
Alt sınıflandırmaya benzer ancak aynı olmayan bir şey sağlamak için türleri diğer türlerin içine yerleştirmenin yolları da vardır.
Üstelik Go'daki methodlar C++ veya Java'daki yöntemlerden daha geneldir: düz, "unboxed" tamsayılar gibi yerleşik türler dahil olmak üzere her türlü veri için tanımlanabilirler. Structlarla sınırlı değillerdir.

<br>

Ayrıca tür hiyerarşisinin olmaması, Go'daki "nesnelerin" C++ veya Java gibi dillere göre çok daha hafif olmasına neden olur.