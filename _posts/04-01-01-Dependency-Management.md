# Bağımlılık Yönetimi {#dependency_management_title}

Seçmek için tonlarda PHP kütüphanesi, yapısı(frameworks) ve bileşeni bulunmaktadır. Projeniz bunlardan birkaçını kullanacaktır - bu proje bağımlılığıdır. 
Yakın zamana kadar PHP'de bu bağımlılıkları yönetmek için uygun bir yol yoktu. Elle yönetilse bile, `autoloader` endişesi mevcuttu. Artık yok. 

Şu sıralarda PHP için iki büyük paket yönetim sistemi bulunmaktadır. `Composer` ve `PEAR`. Hanigis sizin için doğru? Cevap ikisi de.  

 * **Composer** bir proje için bağımlılıkları yönetmek için kullanılır.
 * **PEAR** PHP'nin bütün sisteminin bağımlılığı için kullanılır. 

Genelde, `Composer` paketleri projeler içerisinde uygun iken, bir PEAR paketi bütün PHP projelerinizde kullanılabilir. PEAR 
ilk bakışta kolay bir yaklaşım gibi gelebilir, project-By-Project yaklaşımın bağımlılıklarınız için avantajları vardır.
