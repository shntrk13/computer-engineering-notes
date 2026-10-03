# Bilgisayar Mimarisi

                    BİLGİSAYAR
                        │
        ┌───────────────┼────────────────┐
        │               │                │
       CPU            Bellek          Giriş/Çıkış
    (İşlemci)       (RAM/Cache)       (I/O)
        │               │                │
        │               │                ├── Klavye
        │               │                ├── Mouse
        │               │                ├── Ekran
        │               │                └── Ağ
        │
        ├── ALU
        ├── Control Unit
        ├── Registers
        └── Cache
                        
             ↕
        Anakart / Bus
             ↕
      Depolama Birimleri
       SSD / HDD

## Transistörler 
Elektrik sinyallerini kontrol eder ve bilgisayarın hesaplama yapmasını sağlayan temel elemanlardır.CPU milyonlarca transistörün birbirine bağlanmasıyla oluşur.

## CPU(Merkezi İşlem Birimi)
Bilgisayarın beyni olarak adlandırılan CPU, talimatları yürütür,hesaplamalar yapar ve verileri yönetir.CPU'nun birden fazla çekirdeği(core) olabilir ve her çekirdek belirli işlemleri bağımsız olarak gerçekleştirebilir.

### ALU(Aritmetik Mantık Birimi)
Aritmetik ve mantıksal işlemleri gerçekleştiren CPU bileşenidir.Toplama,Çıkarma,VE,VEYA,DEĞİL gibi işlemleri gerçekleştirir.

### Control Unit
Bilgisayar mimarisinin tüm bileşenlerini kontrol eder.ALU'e veri aktarıp,veri alır ve böylece her bileşenin nasıl davranacağını bilir.

### Register
CPU'nun komutları yürütürken doğrudan kullandığı bilgileri geçici olarak tutan küçük ve çok hızlı depolama alanıdır.RAM CPU'ya uzak olduğu için CPU'nun işlem sırasında kullanacağı bilgileri registerda geçici olarak tutup kullanması işlemi hızlandırır.

### Cache(Önbellek)
L1,L2,L3 seviyelerine ayrılır.CPU'nun sık ihtiyaç duyduğu veya yakın zamanda kullanması muhtemel verileri CPU'ya daha yakın tutarak RAM'e erişim ihtiyacını azaltmak.Registorla aynı şey değildir.L1 en küçük ama en hızlısı L3 en büyüğü ama en yavaşı.L1 genellikle CPU çekirdeğine çok yakındır.

**Register or Cache** 
Register CPU'nun yaptığı işlemin ihtiyaç duyduğu küçük miktardaki verileri tutar.Cache,RAM'deki daha büyük veri ve komut bloklarını CPU'ya yakın bir kopyasını tutarak bellek erişim gecikmesini azaltır.

## GPU(Grafik İşlem Birimi)
CPU tüm hesaplamaları yaparken GPU görselle ilgilenir.Çok sayıda işlemi paralel gerçekleştirmede güçlüdür.

**GPUsuz bir bilgisayar çalışabilir.Ancak CPU'nun gerçekleştirdiği basit grafik işlemler dışında ekran görüntüsü oluşturamaz.**

## Memory
- Birincil Bellek:İşlemciyle doğrudan iletişim kurabilen tek bellektir.İki türü vardır.
     1-RAM
     2-ROM(sistemin çalışması için kullanılan verileri depolar.Bu verilerin önemi nedeniyle bilgisayar kapalıyken bile bilgileri saklar.)
- İkincil Bellek:Daha büyük miktardaki(ve kalıcı verileri) saklamak için yer sağlar.Daha yavaştır.

## RAM(Random Access Memory)
Bilgisayarın kısa süreli ve geçici veri depolama alanıdır.Bilgisayarın işlem yapmak için ihtiyaç duyduğu bilgilerin sasklandığı yerdir.Bilgisayar çalışırken işlemci programlar ve açık dosyalar için gerekli veri RAM'e yüklenir.Bu sayede işlemci verilere hızlıca ulaşır.Ancak bilgisayar kpaatıldığında RAM'deki veriler kaybolur çünkü RAM volatil(geçici) bellektir.

## HDD(Hard Disk Drive)
Bilgisayarın kalıcı belleğini sağlar.SSD'ye göre yavaştır ama veri depolama kapasitesi büyük dosya koleksiyonlarını taşımak için idealdir.

## SSD
Verileri kalıcı olarak saklamak için kullanılır.Hızlı veri erişimi sağlar ve bilgisayarın performansını arttırır.HDD'ye göre daha sessiz,daha hızlıdır.

## Anakart
Bilgisayarın CPU,RAM,Ekran Kartı(GPU),depolama aygıtları gibi donanımlar anakart üzerinde yer alır ve iletişimi sağlar.

## Bus
Bilgisayarın parçalarının birbiriyle veri iletişiminde kullanılan bağlantı yollarına bus(veri yolu) denir.CPU diğer bileşenlerle bus yollarıyla iletişim kurar.Bus verileri taşıyan fiziksel sinyal hatlarıdır.

## Input Devices
- Klavye 
- Fare (Mouse) 
- Ekran 
- Scanner
- Mikrofon
- Kamera

## Output Devices 
Bilgisayarın İşlediği verileri kullanıcıya ya da başka cihaza iletmesini sağlar.
- Monitör
- Yazıcı
- Hoparlör & Kulaklık
- Projeksiyon Cihazı
