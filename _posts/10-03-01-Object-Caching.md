---
isChild: true
---

## Nesnel Önbellekleme {#object_caching_title}

Veritabanından çağırmanın veya verinin getirilmesinin masraflı olduğu ve verinin değişmediği durumlar gibi kodunuzda 
bireysel nesneleri önbelleklemenin yararlı olabileceği zamanlar vardır. Bu verileri bellekte tutmak ve daha sonra 
hızlıca erişmek için nesnel önbellekleme yazılımlarını kullanabilirsiniz. Veritabanı sunucusuna binen yükü  
azaltarak performansı artırabilirsiniz. 

Birçok popüler Bytecode Cache çözümü özel verilerinizi önbelleklemenize izin verir, _so there's even more reason to take
advantage of them._ APC, XCache, ve WinCache PHP verilerinizi önbelleklemek için bir arayüz (API) sunar. 

En genel kullanılan nesnel önbellekleme sistemleri APC ve memcached'dır. APC mükkemmel bir seçimdir, belleğe erişmek
için, basit bir arayüze sahiptir. Kolay kurulabilirdir ve kullanılabilirdir. APC'nin bir sınırılaması sunucuda yüklü 
bulunmasıdır. Memcached ise ayrılmış bir servis olarak kurulur ve network üzerinden kullanılır, bunun anlamı br çok 
farklı sistemden erişebileceğiniz merkezi bir süper hızlı veri depolama imkanı sağlamasıdır. 

PHP (Fast-)CGI olarak sunucunuzda çalışıyorsa, her işlem kendi önbelleğini kullanacaktır. APC verileri işlemler 
arasında paylaşılmayacaktır. Bu durumda, memcached kullanmayı tercih edebilirsiniz, memcached PHP işleme sürecine 
bağlı değildir. 

Bir ağ yapılandırmasında APC memcached'dan erişim hızı açısından genellikle daha iyi performans gösterecektir, 
ama memcached daha hızlı ve daha fazla büyümek için uygun olacaktır. Eğer uygulamanızın ekstra özelliklerini veya 
birden fazla sunucuda çalışmasını önemsemiyorsanız, memcached APC'den nesnel önbellekleme için daha iyi bir seçimdir.

APC örneği:

{% highlight php %}
<?php
// veri 'expensive_data' olarak önbelleklenmişmi diye kontrol et
$data = apc_fetch('expensive_data');
if ($data === false) {
    // veri önbellekte değil; sonucu sonradan çağırmak için önbelleğe kaydet. 
    apc_add('expensive_data', $data = get_expensive_data());
}

print_r($data);
{% endhighlight %}

Nesnel önbellekleme sistenleri hakkında daha fazla bilgi:

* [APC Fonksiyonları](http://php.net/manual/tr/ref.apc.php)
* [Memcached](http://memcached.org/)
* [Redis](http://redis.io/)
* [XCache APIs](http://xcache.lighttpd.net/wiki/XcacheApi)
* [WinCache Fonksiyonları](http://www.php.net/manual/en/ref.wincache.php)
