# Neden Go, methodlarda ve operatörlerde *overloading*i desteklemiyor ?

Tip eşleştirmesi de gerekmiyorsa method çağırımı basitleştirilmiştir.
Diğer dillerdeki deneyimlerimiz bize, aynı adla ancak farklı imzalarla çeşitli methodlara sahip olmanın bazen yararlı olduğunu ancak pratikte bunun kafa karıştırıcı ve kırılgan olabileceğini de gösterdi.
Yalnızca isme göre eşleştirme yapmak ve parametrelerde tür tutarlılığı sağlamak, Go'nun yazım sisteminde önemli bir basitleştirici karardı.

<br>

Operatörlerde overloading ile ilgili olarak, bu mutlak bir gereklilikten çok kolaylık gibi görünüyor.  Tekrar olarak: overloading olmadan her şey daha basit.