# İşletim Sistemi Temelleri

İşletim sistemi, bilgisayarın donanımı ile üzerinde çalışan programlar arasında bağlantı kuran temel yazılımdır. Bilgisayarı açtığımızda arka planda birçok işlemi işletim sistemi yönetir. Örneğin RAM’in kullanılması, çalışan programların işlemciye erişmesi ve dosyaların depolama biriminden okunması işletim sistemi tarafından yönetilir.

## Kernel (Çekirdek)

Kernel, işletim sisteminin en önemli bölümlerinden biridir. Donanım ile programlar arasındaki iletişimi sağlar.

Örneğin bir program klavyeden bir veri almak istediğinde doğrudan klavyenin donanımına erişmek yerine işletim sistemi üzerinden bu işlemi gerçekleştirir. Kernel burada gerekli işlemleri yapar.

Kernel’in temel görevlerinden bazıları:

* İşlemciyi yönetmek
* RAM kullanımını yönetmek
* Çalışan programları yönetmek
* Donanımlarla iletişim kurmak
* Dosya sistemleri ile çalışmak

Kısaca kernel, işletim sisteminin donanım tarafını yöneten bölümüdür.

## Process (İşlem)

Process, çalışan bir programın işletim sistemi tarafından oluşturulan halidir.

Örneğin bilgisayarda Chrome’u açtığımızda işletim sistemi Chrome için bir process oluşturur. Bu process’in kendisine ait bir bellek alanı ve bazı kaynakları vardır.

Bir program çalışırken birden fazla process oluşturabilir. İşletim sistemi bu process’leri takip eder ve hangi işlemin ne zaman çalışacağını belirler.

## Thread (İş Parçacığı)

Thread, bir process içerisindeki daha küçük çalışma birimidir.

Bir process’in içerisinde birden fazla thread bulunabilir. Bu sayede program aynı anda birden fazla işi gerçekleştirebilir.

Örneğin bir internet tarayıcısında bir thread sayfanın yüklenmesiyle ilgilenirken başka bir thread kullanıcı işlemleriyle ilgilenebilir.

Process ve thread arasındaki temel farkı şu şekilde düşünebiliriz:

|Process |	Thread|
|---|---|
|Çalışan programdır.|	Process içerisindeki çalışma birimidir.|
|Kendine ait bellek alanı vardır.|	Aynı process’in belleğini paylaşabilir.|
|Oluşturulması daha maliyetlidir.| Oluşturulması daha az maliyetlidir.|
|Birden fazla thread içerebilir.|	Bir process içerisinde çalışır.|

## Bellek Yönetimi

İşletim sisteminin görevlerinden biri de RAM’i yönetmektir. Bilgisayarda aynı anda birçok program çalışabildiği için RAM’in hangi program tarafından ne kadar kullanılacağını işletim sistemi belirler.

Örneğin aynı anda bir tarayıcı, VS Code ve müzik uygulaması açık olduğunda bu programların hepsi RAM kullanır. İşletim sistemi bu kaynakların programlar arasında düzenli şekilde kullanılmasını sağlar.

### Virtual Memory (Sanal Bellek)

RAM yetersiz kaldığında işletim sistemi depolama alanının bir kısmını RAM gibi kullanabilir. Buna sanal bellek denir.

Ancak SSD veya HDD RAM’den daha yavaş olduğu için sanal belleğin kullanılması bilgisayarın yavaşlamasına neden olabilir.

## CPU Scheduler

Bilgisayarda aynı anda birçok process çalışabilir. Fakat işlemci her işlemi aynı anda gerçekleştiremeyeceği için hangi process’in ne zaman çalışacağını belirlemek gerekir.

Bu görevi CPU scheduler gerçekleştirir.

Scheduler, process’lerin önceliklerini ve çalışma durumlarını değerlendirerek işlemci zamanını dağıtır.

Örneğin bir programın çalışması devam ederken başka bir programın kullanıcının yaptığı işlemlere cevap vermesi gerekiyorsa işlemci zamanını bu programlara paylaştırabilir.

## Sonuç

İşletim sistemini öğrenmek, yazdığımız programların bilgisayarda aslında nasıl çalıştığını anlamamıza yardımcı olur. Bir program çalıştırıldığında arka planda process ve thread’ler oluşturulur, RAM kullanılır ve CPU zamanı işletim sistemi tarafından dağıtılır.

Bu yüzden işletim sistemi konusunu öğrenmek, yazılım ile bilgisayarın donanımı arasındaki bağlantıyı anlamak açısından önemlidir.