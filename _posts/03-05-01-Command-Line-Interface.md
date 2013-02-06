---
isChild: true
---

## Komut Satırı Arayüzü {#command_line_interface_title}

PHP web uygulamaları geliştirmek için oluşturuldu, ama komut satırı (CLI) uygulamaları içinde yararlıdır. Komut Satırından çalışan PHP uygulamaları test etme, yayınlama ve uygulama yönetimi vs gibi uygulamaları otomatize etmenize yardımcı olabilir.

CLI PHP uygulamaları güvenli bir web arayüzü oluşturmadan direk olarak çalıştığı için güçlüdür. Sadece komut satırı uygulamanızı direk ana web anadizinine koymayınız!

Aşağıdaki komutları komut satırında çalıştırmayı deneyiniz : 

{% highlight bash %}
> php -i
{% endhighlight %}

`-i` özelliği PHP'nin konfigürasyonlarını [`phpinfo`][phpinfo] fonksiyonu gibi ekrana bastıracaktır.

`-a` özelliği ise ruby'nin IRBsi veya python gibi interaktif bir kabuk sağlayacaktır. [command line options][cli-options]'dan daha fazla özelliğe ulaşabilirsiniz.

"Hello, $name" yazan basit bir CLI uygulaması yazalım. `hello.php` adında bir dosya oluşturup bunu çalıştırmayı deneyin.

{% highlight php %}
<?php
if ($argc != 2) {
    echo "Usage: php hello.php [name].\n";
    exit(1);
}
$name = $argv[1];
echo "Hello, $name\n";
{% endhighlight %}

PHP kodunuz çalıştığında argümanlar için iki özel değişken oluşturmaktadır. [`$argc`][argc] argümanların *sayısını* içereren sayı(integer) tipinde bir değişkendir ve [`$argv`][argv] her bir argümanın *değerini* içeren değişken dizisidir. İlk argüman her zaman PHP kodunun çalıştırıldığı dosyanın adınıdır, bu örnekte `hello.php`dir. 

`exit()` kodu kabuğun komutun hata ile sonuçlandığını düşünmemesi için sıfır olmayan bir değişken ile kullanılmalıdır. Genelde kullanılan exit  komutları [buradadır][exit-codes].

Kodumuzu çalıştırmak için aşağıdaki satırları kullanabilirsiniz : 

{% highlight bash %}
> php hello.php
Usage: php hello.php [name]
> php hello.php world
Hello, world
{% endhighlight %}


 * [Learn about running PHP from the command line][php-cli]
 * [Learn about setting up Windows to run PHP from the command line][php-cli-windows]

[phpinfo]: http://php.net/manual/en/function.phpinfo.php
[cli-options]: http://www.php.net/manual/en/features.commandline.options.php
[argc]: http://php.net/manual/en/reserved.variables.argc.php
[argv]: http://php.net/manual/en/reserved.variables.argv.php
[php-cli]: http://php.net/manual/en/features.commandline.php
[php-cli-windows]: http://www.php.net/manual/en/install.windows.commandline.php
[exit-codes]: http://www.gsp.com/cgi-bin/man.cgi?section=3&topic=sysexits
