# Ağ Temelleri

Bilgisayar ağları, bilgisayarların ve diğer cihazların birbirleriyle iletişim kurmasını sağlar. Günümüzde kullandığımız internet siteleri, mobil uygulamalar ve birçok yazılım ağ üzerinden veri alışverişi yapar.

Bir programın internette başka bir bilgisayardaki sunucuya bağlanabilmesi için IP, port, DNS ve TCP/UDP gibi bazı temel kavramların bilinmesi gerekir.

## IP Adresi

IP adresi, ağ üzerindeki bir cihazı tanımlamak için kullanılır.

Evimizdeki bilgisayar, telefon veya başka bir cihaz internete bağlandığında bir IP adresine sahip olur. Bir web sitesine bağlanırken de aslında bir sunucunun IP adresine bağlantı kurulur.

Örneğin bir IP adresi şu şekilde olabilir:

192.168.1.10

IPv4 adresleri dört bölümden oluşur ve her bölüm 0 ile 255 arasında bir değer alabilir.

## Port

IP adresi cihazı bulmamıza yardımcı olurken port numarası o cihaz üzerindeki hangi servise veya uygulamaya bağlanacağımızı belirtir.

Örneğin web servislerinde yaygın olarak kullanılan portlardan bazıları:

HTTP  → 80
HTTPS → 443

Bu nedenle bir bağlantıda sadece IP adresini bilmek yeterli değildir. Hangi servise bağlanacağımızı belirlemek için port da önemlidir.

## DNS

DNS, alan adlarını IP adreslerine çevirmek için kullanılan sistemdir.

Örneğin tarayıcıya:

www.google.com

yazdığımızda bilgisayarın bu alan adının hangi IP adresine karşılık geldiğini öğrenmesi gerekir.

DNS bu işlemi gerçekleştirir.

Bu sayede insanların hatırlaması zor olan IP adresleri yerine alan adlarını kullanabiliriz.

## TCP

TCP, internet üzerinde güvenilir veri iletişimi sağlamak için kullanılan bir protokoldür.

TCP ile gönderilen verilerin karşı tarafa ulaşması ve doğru sırada olması kontrol edilir. Eğer bir veri kaybolursa tekrar gönderilmesi sağlanabilir.

Bu nedenle dosya indirme veya web sayfalarına erişme gibi veri kaybının istenmediği durumlarda TCP kullanışlıdır.

## UDP

UDP de ağ üzerinden veri göndermek için kullanılan bir protokoldür. TCP’ye göre daha basit ve hızlıdır ancak gönderilen verilerin kesin olarak ulaştığını kontrol etmez.

Bu nedenle hızın daha önemli olduğu bazı uygulamalarda UDP tercih edilebilir.

Örneğin online oyunlarda ve bazı canlı yayın uygulamalarında UDP kullanılabilir.

### TCP ve UDP Karşılaştırması

|TCP| UDP|
|---|---|
|Güvenilir iletişim sağlar.|	Hızlı iletişim sağlar.|
|Paketlerin ulaşmasını kontrol eder.|	Paketlerin ulaşmasını garanti etmez.|
|Paketlerin sırasını kontrol eder.|	Sıra kontrolü yapmaz.|
|Daha fazla kontrol mekanizmasına sahiptir.|	Daha basittir.|

## Paket Yapısı

Ağ üzerinden gönderilen bilgiler tek parça halinde değil, paketler halinde gönderilir.

Bir paket içerisinde genel olarak gönderen ve alıcı hakkında bilgiler, kullanılan protokol ve taşınan veri bulunabilir.

Basit olarak bir paketi şu şekilde düşünebiliriz:

+----------------------+
| Kaynak Bilgisi       |
+----------------------+
| Hedef Bilgisi        |
+----------------------+
| Protokol Bilgisi     |
+----------------------+
| Veri                 |
+----------------------+

Gönderilen veri bu paketler üzerinden ağ içerisinde taşınır ve hedef bilgisayarda tekrar işlenir.

### ping Komutu

ping, bir bilgisayara veya sunucuya ulaşılabilir olup olmadığını kontrol etmek için kullanılan bir komuttur.

Örneğin:

ping google.com

komutuyla Google sunucusuna ulaşmaya çalışabiliriz.

Ping sonucunda cevap süresi gibi bilgiler görülebilir. Bu değer genellikle milisaniye cinsinden gösterilir.

### traceroute

traceroute, bilgisayarımızdan hedef sunucuya giderken verilerin geçtiği ağ noktalarını görmek için kullanılır.

Windows’ta bunun karşılığı genellikle:

tracert google.com

şeklindedir.

Bu komut sayesinde bağlantının hangi noktalardan geçtiği hakkında bilgi elde edebiliriz.

### nslookup

nslookup, bir alan adının DNS kayıtlarını ve IP adresini öğrenmek için kullanılabilir.

Örneğin:

nslookup google.com

komutuyla alan adının hangi IP adreslerine karşılık geldiğini görebiliriz.

## Sonuç

Ağ temellerini öğrenmek, yazdığımız programların internet üzerinden nasıl iletişim kurduğunu anlamamızı sağlar.

IP adresi cihazın bulunmasına, port hangi servise bağlanacağımızı belirlemeye, DNS alan adlarını IP adreslerine çevirmeye yardımcı olur. TCP ve UDP ise verilerin ağ üzerinden nasıl taşınacağını belirleyen önemli protokollerdir.

ping, traceroute ve nslookup gibi komutlar da ağ bağlantısını kontrol etmek ve sorunları anlamak için kullanılabilir.