---
title: Kodlama Stili Rehberi
---

# Kodlama Stili Rehberi  {#kodlama_stil_rehberi_title}

PHP topluluğu geniş ve çeşitlidir, sayısız kütüphane, framework ve bileşenlerden oluşur. Bunlardan birkaçını seçip bir 
projede kullanmak bir PHP geliştiricisi için normaldir. PHP kodunda genel bir stile uymak farklı ve çeşitli 
kütüphaneleri kullanmak ve karşılaştırmak açısından geliştiriciler için önemlidir. PHP kodunun genel kod stiline 
olabildiğince uyması gerekiyor ki geliştiriciler kolaylıkla farklı kütüphaneleri karıştırıp eşleştirebilsinler.

[Framework Interop Group][fig] (daha önce 'PHP Standards Group' olarak bilinen) çeşitli kodlama standartları önerilerinde bulunmuş ve [PSR-0][psr0], [PSR-1][psr1], [PSR-2][psr2] ve [PSR-3][psr3] olarak bilinen standartları kabul etmiştir. Kabul edilmiş olan bu standartlar Drupal, Zend, Symfony, CakePHP, phpBB, AWS SDK, FuelPHP, Lithium gibi büyük projelerde kullanılmaya başlanmıştır. Bunları kendi projelerinizde kullanabilirsiniz veya kendi kodlama stilinizi ve standartlarınız ile devam edebilirsiniz.

Diğer geliştiricilerin daha kolya okuyup ve üzerinden çalışabilmesi için siz bu standartlardan bir veya daha fazlasına 
uygun kod yazmalısınız, ve üçüncü parti kodlarla çalışırken bir çok bileşenden oluşan uygulamalar birbiri ile daha 
uyumlu olabilir. İlk öneri önceki önerileri içerecek şekilde tasarlanmıştır. 

* [PSR-0 hakkında][psr0]
* [PSR-1 hakkında][psr1]
* [PSR-2 hakkında][psr2]
* [PSR-3 hakkında][psr3]

[PHP_CodeSniffer][phpcs] kullanarak yazdığınız kodları çeşitli standartlar ve stiller üzerinde kontrol edebilirsiniz. 
Fabien Potencier tarafından hazırlanan [PHP Coding Standards Fixer][phpcsfixer] uygulamasını kullanarak kodlarınızın bu standartlara uygun olarak otomatik düzeltilmesini sağlayabilirsiniz.

İngilizce dili kod içinde bulunan değişken, sabit, fonksiyon, yordam gibi semboller ve yapılara ait isimlendirmelerde tercih edilir. Yorumlar için ise şu anda ve gelecekte kodlar üzerinde uğraşacak kişilerin anlayabileceği bir dil tercih edilebilir (Örneğin; proje ekibinde yabancı veya Türkçe bilmeyen bir eleman varsa Türkçe yerine İngilizce tercih etmeniz daha uygun olur).


[fig]: http://www.php-fig.org/
[psr0]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md
[psr1]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-1-basic-coding-standard.md
[psr2]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md
[psr3]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-3-logger-interface.md
[phpcs]: http://pear.php.net/package/PHP_CodeSniffer/
[phpcs-psr]: https://github.com/klaussilveira/phpcs-psr
[phpcsfixer]: http://cs.sensiolabs.org/

