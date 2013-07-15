---
title: Bytecode Cache (Önbelleği)
isChild: true
---

## Bytecode Cache (Önbelleği) {#bytecode_cache_onbellegi_title}

PHP dosyaları çalıştırıldığı zaman, kodlar ilk olarak bytecode'a (aynı zamanda opcode olarak bilinir) derlenir ve daha sonra bytecode çalıştırılır. 
Eğer PHP değiştirilmemişse, bytecode her zaman aynıdır.  Bunun anlamı derleme aşaması CPU kaynaklarını boşa zaman harcamak demektir.

Bytecode gereksiz derlemeleri önlemek için bellekte saklanacaktır ve oradan çağırılacaktır. Kurulumu ve ayarlamaları sadece dakikalar alırken uygulamanız önemli ölçüde hızlanacaktır. Kurmamanız için hiç bir neden yok. 

Popüler bytcode önbellek araçları:

* [APC](http://php.net/manual/tr/book.apc.php)
* [XCache](http://xcache.lighttpd.net/)
* [Zend Optimizer+](http://www.zend.com/products/server/) (part of Zend Server package)
* [WinCache](http://www.iis.net/download/wincacheforphp) (extension for MS Windows Server)
