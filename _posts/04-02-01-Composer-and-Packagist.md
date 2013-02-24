---
title: Composer ve Packagist
isChild: true
---

## Composer ve Packagist {#composer_ve_packagist_title}

Composer PHP için **muhteşem** bir bağımlılık yönetimi aracıdır. Bağımlılık yönetimini bir kaç basit komut ile `composer.json` dosyası içerisinde yazıyoruz, Composer projenizin ihtiyaçlarını otomatik olarak indiriyor ve kurulumunu gerçekleştiriyor.

Composer ile uyumlu şimdiden projenizde kullanmanız için bir çok PHP kütüphanesi bulunmakta. Bu paketler Composer'ın resmi deposu olan [Packagist][1]'da listelenmetedir.

### Composer Nasıl Kurulur

Yerel (önerilmemesine rağmen içinde bulunduğunuzu dizin için) ya da genel (örneğin: /usr/local/bin) kullanım için Composer'ı kurabilirsiniz. Yerel olarak kurmak için aşağıdaki örneğe bakınız:

    curl -s https://getcomposer.org/installer | php

Bu komut `composer.phar` (bir PHP ikili arşivi) dosyası indirecek. Bu dosyayı `php` kullanarak çalıştırabilir ve projenizin ihtiyaçlarını yönetebilirsiniz. <strong>Not:</strong> Kodu çevirici bir kaynağa indirdi iseniz öncelikle çevrim içi kod okuyunuz.

### Composer Nasıl Kurulur (elle)

Composer'i elle kurmak biraz üst seviye bir tekniktir. Ancak geliştiricinin etkileşimli kurulum yerine bu yöntemi kullanması için bir kaç sebep vardır. Etkilşimli kurulum aşağıdaki PHP kurulumlarını denetler:

 - PHP'nin yeterli bir sürümü kontrol edilir
 - `.phar` dosyası düzgün çalıştırılır.
 - Dizin izinleri kontrol edilir.
 - Sorunlu uzantılar yüklenmez.
 - Belirli `php.ini` ayarları ayarlanır. 

Bu kurulum adımlarının hiçbiri olmadan yapılan elle kurulumda, sizin için bir değerinin olup olmadığına karar vermelisiniz. Aşağıdaki komutlar ile elle kuruluma başlayalım : 

    curl -s https://getcomposer.org/composer.phar -o $HOME/local/bin/composer
    chmod +x $HOME/local/bin/composer

`$HOME/local/bin` dizini (ya da sizin seçeceğiniz bir dizin) sizin `$PATH` değişkeninizin içerisinde olmalı. Bu `composer` komutunu kullanılabilir yapacaktır. 

Dökümantaasyonda karşılaştığımız `php composer.phar install` komutunu aşağıdaki gibi kullanabilirsiniz : 

    composer install

### Bağımlıklıkları Nasıl Tanımlar ve Kurarız

İlk olarak `composer.json` dosyasını `composer.phar` ile aynı dizinde oluşturuyoruz. Aşağıda [Twig][2]'i projemize ekleyelim.

	{
	    "require": {
	        "twig/twig": "1.8.*"
	    }
	}

Daha sonra aşağıdaki komutları projenin ana dizininde çalıştırıyoruz.

    php composer.phar install

Bu projenin bağımlı olduğu projeleri `vendors/` dizinine indirecektir ve kuracaktır. Daha sonra aşağıdaki satırları uygulamanızın ana PHP dosyasına ekleyiniz; bunları nasıl yapacağınız size zaten Composer'daki projelerde bildirilecek.

{% highlight php %}
<?php
require 'vendor/autoload.php';
{% endhighlight %}

Şimdi projenize eklediğiniz kütüphaneleri kullanabilirsiniz ve bunlar projenizde talep dahilinde otomatik yükleniyor (autoloaded) olacak.

* [Composer hakkında][3]

[1]: http://packagist.org/
[2]: http://twig.sensiolabs.org
[3]: http://getcomposer.org/doc/00-intro.md
