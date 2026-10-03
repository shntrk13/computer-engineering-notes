# Dosya Sistemleri ve Depolama Mantığı

Bilgisayarda oluşturduğumuz dosyaların depolama biriminde düzenli bir şekilde tutulması gerekir. İşletim sistemi bu dosyaları kaydetmek, okumak, silmek ve düzenlemek için bir dosya sistemi kullanır.

Dosya sistemi, depolama alanındaki verilerin nasıl organize edileceğini belirleyen yapıdır.

Farklı işletim sistemlerinde farklı dosya sistemleri kullanılabilir. Bunlardan bazıları NTFS, ext4 ve APFS’dir.

## NTFS

NTFS, özellikle Windows işletim sistemlerinde kullanılan bir dosya sistemidir.

Dosyaların ve klasörlerin düzenli bir şekilde saklanmasını sağlar. Ayrıca dosya izinleri ve güvenlik gibi özellikleri destekler.

Windows bilgisayarlarda kullanılan disklerde NTFS ile sıkça karşılaşabiliriz.

### ext4

ext4, Linux sistemlerinde yaygın olarak kullanılan dosya sistemlerinden biridir.

Büyük miktarda verinin düzenli şekilde saklanmasını ve yönetilmesini sağlar. Linux tabanlı işletim sistemlerinde uzun süredir kullanılan dosya sistemlerinden biridir.

## APFS

APFS, Apple tarafından geliştirilen bir dosya sistemidir.

Özellikle macOS gibi Apple işletim sistemlerinde kullanılır. SSD’ler için optimize edilmiş özelliklere sahiptir.

### Dosya Sistemlerinin Karşılaştırılması

|Dosya Sistemi|	Genellikle Kullanıldığı Sistem|
|---|---|
|NTFS|	Windows|
|ext4 |Linux|
|APFS|	macOS / Apple cihazları|

## Block (Blok) Yapısı

Depolama alanındaki veriler tek bir büyük alan olarak tutulmaz. Depolama alanı çeşitli küçük bölümlere ayrılarak kullanılabilir.

Bu bölümlere genel olarak blok adı verilebilir.

Bir dosya oluşturduğumuzda dosyanın verileri gerekli bloklara yazılır. Dosya sistemi de bu verilerin hangi bloklarda bulunduğunu takip eder.

Basit olarak şöyle düşünebiliriz:

Depolama Alanı

```text
+-------+-------+-------+-------+
| Blok  | Blok  | Blok  | Blok  |
|   1   |   2   |   3   |   4   |
+-------+-------+-------+-------+
```
Bir dosya birden fazla bloğa ihtiyaç duyuyorsa verileri birden fazla blokta bulunabilir.

## HDD Nasıl Çalışır?

HDD, verileri manyetik diskler üzerinde saklayan bir depolama birimidir.

HDD’nin içerisinde dönen plakalar ve bu plakalar üzerindeki verileri okuyup yazan bir kafa bulunur.

Veriye ulaşmak için fiziksel olarak hareket eden parçalar bulunduğu için HDD’lerde erişim süresi SSD’lere göre daha uzundur.

HDD’nin avantajlarından biri yüksek depolama kapasitesini daha uygun fiyatla sunabilmesidir.

## SSD Nasıl Çalışır?

SSD’lerde HDD’den farklı olarak hareket eden mekanik parçalar bulunmaz.

Veriler flash bellek hücrelerinde saklanır. Bu nedenle SSD’ler genel olarak HDD’lerden daha hızlıdır.

SSD’lerin hareketli parçası olmadığı için sessiz çalışmaları da önemli avantajlarından biridir.

### HDD ve SSD Karşılaştırması

|HDD|	SSD|
|---|---|
|Mekanik parçalar kullanır.|	Hareketli parça içermez.|
|Daha yavaştır.|	Daha hızlıdır.|
|Daha uygun fiyatlı olabilir.|	Genellikle daha pahalıdır.|
|Çalışırken ses çıkarabilir.|	Sessiz çalışır.|
|Fiziksel darbelere karşı daha hassastır.|	Mekanik parça olmadığı için daha dayanıklıdır.|

## Veri Okuma ve Yazma

Bir dosyayı açtığımızda bilgisayarın depolama birimindeki verileri bulup okuması gerekir.

Basit olarak işlem şu şekilde gerçekleşebilir:

Kullanıcı
   ↓
İşletim Sistemi
   ↓
Dosya Sistemi
   ↓
Depolama Birimi
   ↓
Dosya Verisi

Dosya sisteminin burada önemli bir görevi vardır. Dosyanın nerede bulunduğunu takip ederek işletim sisteminin gerekli verilere ulaşmasına yardımcı olur.

Dosya yazarken de benzer şekilde işletim sistemi ve dosya sistemi birlikte çalışır ve veriler uygun depolama alanlarına kaydedilir.

## Sonuç

Dosya sistemleri, bilgisayardaki verilerin düzenli şekilde saklanmasını ve yönetilmesini sağlar. NTFS, ext4 ve APFS farklı işletim sistemlerinde kullanılan önemli dosya sistemleridir.

HDD ve SSD ise verilerin fiziksel olarak saklandığı farklı depolama teknolojileridir. HDD mekanik parçalara sahipken SSD flash bellek kullanır. Bu nedenle SSD’ler özellikle veri okuma ve yazma işlemlerinde daha hızlıdır.

Bu konuları öğrenmek, bilgisayarda bir dosyanın kaydedilmesi veya açılması sırasında arka planda neler olduğunu anlamamıza yardımcı olur.