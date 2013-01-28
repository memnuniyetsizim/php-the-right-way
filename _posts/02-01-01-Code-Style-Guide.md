# Kod Stil Rehberi  {#code_style_guide_title}

PHP topluluğu geniş ve çeşitlidir, sayısız kütüphane, framework ve bileşenlerden oluşur. Bunlardan birkaçını seçip bir 
projede kullanmak bir PHP geliştiricisi için normaldir. PHP kodunda genel bir stile uymak farklı ve çeşitli 
kütüphaneleri kullanmak ve karşılaştırmak açısından geliştiriciler için önemlidir.

It is important that PHP code adhere (as close as possible) to a common code style to make it easy for developers to 
mix and match various libraries for their projects.

[Framework Interop Group][fig] (PHP Standartlar Grubu), [PSR-0][psr0], [PSR-1][psr1], [PSR-2][psr2] and [PSR-3][psr3] 
olarak bilinen, bir dizi önerilmiş ve kabul görmüş önerilerdir. Komik isimler ile karıştırmayın(!), Bu öneriler Drupal, 
Zend, CakePHP, phpBB, AWS SDK, FuelPHP, Lithium, ... vb. projeler tarafından benimsenmeye başlanan bir 
dizi kurallardır. Kendi projelerinizde veya kendi kişisel stiliniz olarak kullanabilirsiniz.

Diğer geliştiricilerin daha kolya okuyup ve üzerinden çalışabilmesi için siz bu standartlardan bir veya daha fazlasına 
uygun kod yazmalısınız, ve üçüncü parti kodlarla çalışırken bir çok bileşenden oluşan uygulamalar birbiri ile daha 
uyumlu olabilir. İlk öneri önceki önerileri içerecek şekilde tasarlanmıştır. 

* [Read about PSR-0][psr0]
* [Read about PSR-1][psr1]
* [Read about PSR-2][psr2]
* [Read about PSR-3][psr3]

Kodunuzu önerilere karşı kontrol etmek için [PHP_CodeSniffer][phpcs] kullanabilirsiniz.
Kodunuzun sentaksındaki prblemleri elle düzenleme zamanından kurtulmak ve otomatik olarak düzenlemek için bu 
standartları içeren "Fabien Potencier [PHP Coding Standards Fixer][phpcsfixer]" i kullanabilirsiniz. 

İngilizce tüm kod altyapısı ve semboller isimleri için tercih edilmektedir. Yorumlar kod üzerinden çalışan 
herkes tarafından kolayca okunabilecek istenilen dillerde yazılabilir.

[fig]: http://www.php-fig.org/
[psr0]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md
[psr1]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-1-basic-coding-standard.md
[psr2]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md
[psr3]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-3-logger-interface.md
[phpcs]: http://pear.php.net/package/PHP_CodeSniffer/
[phpcs-psr]: https://github.com/klaussilveira/phpcs-psr
[phpcsfixer]: http://cs.sensiolabs.org/

