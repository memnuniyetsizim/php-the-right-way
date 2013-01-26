---
isChild: true
---

## Vagrant {#vagrant_title}

Deliştirme ortamı ile yayınlama ortamınız fakrlı ise projenizi yayınladığınızda değişik hatalar ile 
karşılaşabilirsiniz. Bir takım ile çalışıyorken farklı geliştirme ortamlarında tüm kütüphanelerin aynı 
versiyonda güncel olabilmesi çok zorlaşıyor.

Eğer Wİndows bir makinede geliştirme yapıp Linux bir makinede yayınlıyorsanız veya bir takım ile geliştiryorsanız, 
bir sanal makine kurmayı düşünmelisiniz. Bu zor gelebilir, ama [Vagrant][vagrant] kullanarak basit bir kaç adım 
ile sanal bir makine kurabilirsiniz. Bu temel box'lar elle ayarlanabilir, veya bunu yapmak için [Puppet][puppet] 
veya [Chef][chef] gibi "provisioning" yazılımları kullanabilirsiniz. Provisioning, birbirleri ile özdeş birden 
fazla box kurulurken ve gerektiğinde silinirken, tekrarlanacak olan bir çok kurulum karmaşasından korunmak 
için güzel bir yöntemdir. Bir box'ı silebilir ve hiç bir manuel yöntem kullanmadan tekrar oluşturabilirsiniz, 
güzel bir kurulumu size sağlar. 

Vargant kodlarınızı sunucu ya da sanal makine ile paylaşmanız için paylaşımlı bir klasör oluşturur. Bunun anlamı 
siz sunucu makinedeki dosyalar yaratabilir ya da editleyebilirsiniz ve sonra sanal makinede bu kodları 
çalıştırabilirsiniz.  

[vagrant]: http://vagrantup.com/
[puppet]: http://www.puppetlabs.com/
[chef]: http://www.opscode.com/
