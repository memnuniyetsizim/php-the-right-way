---
isChild: true
---

## Programlama Paradigmaları {#programming_paradigms_title}

PHP çeşitli programlama tekniklerini destekleyen esnek ve dinamik bir dildir. 
özellikle PHP 5.0 da katı bir nesne tabanlı model ekleyerek (2004), PHP 5.3 de "anonymous functions" ve "namespaces" 
(2009) ve PHP 5.4'de "traits" ekleyerek yıllar içerisinde önemli ölçüde gelişti.

### Nesne Tabanlı Programlama

PHP nesne tabanlı programlamanın "class", "abstract class", "interfaces", "inheritance", "constructors", "cloning", 
"exception" ve daha fazlası bütün özelliklerini içermektedir


* [Read about Object-oriented PHP][oop]
* [Read about Traits][traits]

### Fonksiyonel Programlama

PHP, bir fonskiyonun bir değişkene atandığı "first-class" fonksiyonu, desteklemektedir. Kullanıcı tanımlı ve dahili 
fonksiyonların ikiside bir değişkene referans edilebilir ve dinamik olarak çağırılabilir. Fonksiyon bir diğer fonksiyona 
parametre olarak gönderilebilir (bu özellik "High-order functions olarak bilinir.") veya bir fonksiyondan geri döndürülebilirler.

Özyineleme(recursion), kendi kendini çağıran fonksiyon desteklenen bir özelliktir, ama bir çok PHP kodu iterasyona odaklanmaktadır.

Yeni anonymous fonksiyonları (closures için desteklenmektedir) PHP 5.3 ile gelmektedir. (2009)

PHP 5.4 added the ability to bind closures to an object's scope and also improved support for callables such that they
can be used interchangeably with anonymous functions in almost all cases.

* [Functional Programming in PHP](/pages/Functional-Programming.html) 
* [Read about Anonymous Functions][anonymous-functions]
* [Read about the Closure class][closure-class]
* [More details in the Closures RFC][closures-rfc]
* [Read about Callables][callables]
* [Read about dynamically invoking functions with `call_user_func_array`][call-user-func-array]

### Meta Programlama

PHP Reflection API ve Magic Method gibi mekanizmalar aracılığıyla meta programlamayı desteklemektedir.
`__get()`, `__set()`, `__clone()`, `__toString()`, `__invoke()`, gibi bir çok sihirli yöntemler (Magic Methods) vardır 
ve bunlar geliştiriciye sınıfaların davranışlarını değiştirmelerine izin verirler. Ruby geliştiricileri genellikler 
PHP'de `method_missing`in eksik olduğunu söylerler, ancak o  `__call()` ve `__callStatic()` olarak mevcuttur.

* [Read about Magic Methods][magic-methods]
* [Read about Reflection][reflection]

[namespaces]: http://php.net/manual/en/language.namespaces.php
[overloading]: http://php.net/manual/en/language.oop5.overloading.php
[oop]: http://www.php.net/manual/en/language.oop5.php
[anonymous-functions]: http://www.php.net/manual/en/functions.anonymous.php
[closure-class]: http://php.net/manual/en/class.closure.php
[callables]: http://php.net/manual/en/language.types.callable.php
[magic-methods]: http://php.net/manual/en/language.oop5.magic.php
[reflection]: http://www.php.net/manual/en/intro.reflection.php
[traits]: http://www.php.net/traits
[call-user-func-array]: http://php.net/manual/en/function.call-user-func-array.php
[closures-rfc]: https://wiki.php.net/rfc/closures
