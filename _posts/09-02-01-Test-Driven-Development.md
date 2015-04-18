---
title: Test Odaklı Geliştirme
isChild: true
---

## Test Odaklı Geliştirme {#test_odakli_gelistirme_title}

[Wikipedia](http://en.wikipedia.org/wiki/Test-driven_development)'den:

Test odaklı geliştirme (TOG) geliştirme döngüsünün küçük bir kısmının tekrarına dayana bir yazılım geliştirme sürecidir: ilk olarak geliştirici istenen bir özelliği ya da fonksiyonu tanımlayan (başlangıçta başarısız) bir test durumunu oluşturur, sonra testi geçmek için az sayıda kodlar eklenir ya da çıkarılır ve sonunda yazılımın işlevini ve davranışını değiştirmeden iç yapısında yapılan değişikliklerle yeni kod kabul edilir standartlara uygun bir hale getirilir. _Kent Beck, who is credited with having developed or 'rediscovered' the technique, stated in 2003 that TDD encourages simple designs and inspires confidence_

Uygulamanız için kullanabileceğiniz bir kaç çeşit test yöntemi vardır: 

### Birim Test (Unit Testing)

Unit Testing fonskiyonları, sınıfları ve metodları bir geliştirme döndüsü üzerinden tüm çalışma zamanında çalıştığından emin olmak için bir programlama yaklaşımıdır. Fonskiyonların ve metodların içindeki ya da dışındaki değişkenlerin değerlerini kontrol ederek iç mantığın doğru çalıştığını kontrol edebilirsiniz. Bağımlılık kontrolü ve sahte sınıflar ve taslaklar inşa ederek, bağımlılığı doğrulayabilirsiniz ve bu daha iyi bir test kapsamı için doğru kullanımdır.

Bir sınıf ya da metod oluşturduğunuzda, bu sınıf ya da metodun her bir davranışı için bir birim test oluşturmalısınız. Basit seviyede, yanlış bir argüman gönderdiğinizde hata vereceğinden ve doğru bir argüman gönderdiğinizde çalışacağından emin olmalısınız. Geliştirme döngüsünde bu sınıf ya da metod içerisinde değişiklik olduğunda eski işlevleri umduğumuz gibi çalışacaktır. 

Birim test için diğer bir kullanım açıkkaynağa katkıda bulunmaktır. Bozuk işlevleri göstermek ve sonrasında düzeltmek için bir test yazabilirsiniz. Testi geçebildiğini gösterebilirsiniz. Bir projeyi çalıştırdığınızda gönderilen istekler için testi bir gereklilik olarak önerebilirsiniz. 

[PHPUnit](http://phpunit.de) PHP uygulamaları için birim test yazmak için de-facto test çatısıdır. Buna ek olarak bir kaç alternatif de bulunmaktadır.

* [SimpleTest](http://simpletest.org)
* [Enhance PHP](http://www.enhance-php.com/)
* [PUnit](http://punit.smf.me.uk/)
* [atoum](https://github.com/atoum/atoum)

### Entegrasyon Test (Integration Testing)

[Wikipedia](http://en.wikipedia.org/wiki/Integration_testing)'den:

Entegrasyon testi (bazen entegrasyon ve test olarakta anılır, kısaltılmış hali "I&T"dir.) uygulamanızdaki modüllerin birleştirildiği ve bir grup olarak test edildiği bir test aşamasıdır. Birim test (Unit Test) sonrası ve doğrulama testleri (Validation Testing) öncesi oluşturulur. Entegrasyon testinde birim testi yapılmış modülleri girdi olarak alınır, daha büyük gruplar oluşturacak şekilde birleştirilir, entegrasyon test planında tanımlanan testler uygulanır ve sistem testi için hazır bir şekilde entegra sistem sunulur.

Birim test için kullanılan bir çok araç entegrasyon testi için de kullanılabilir. 


### Fonksiyonel Test (Functional Testing)

(acceptance testing) olarak da bilinen, fonksyonle test birimlerin birbirleri ile doğru konuşup konuşmadığını ve birimlerin tek tek düzgün çalışıp çalışmadığını kontrol etmek yerine uygulamanızı gerçekten kullanan otomatik test araçları oluşturmak için kullanılan araçlar kullanarak oluşturulur. Bu araçlar gerçek veriler ile ve gerçek kullanıcıları simule ederek çalışırlar. 

#### Fonksiyonel Test Araçları

* [Selenium](http://seleniumhq.com)
* [Mink](http://mink.behat.org)
* [Codeception](http://codeception.com) is a full-stack testing framework that includes acceptance testing tools
