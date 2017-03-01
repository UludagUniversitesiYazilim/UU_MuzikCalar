# UÜ MEDYA OYNATICI
Basit bir medya oynatıcı. Öğrenme ve gelişme amaçlıdır. Python için eğitim PDF'si [buradan](http://indir.istihza.com/belgeler/py3/python3.pdf)

**Bu dosya şu an için geliştiricileri hedeflemektedir.**

## Kullanılacak dil

Hemen her programlama diliyle yapılabilir bir uygulama. Daha önce **Python3** olarak seçmiştik ama başlamadığımız için hala tartışmaya açık. Üst menüdeki ISSUE kısmında tartışılabilir. Hemen her dille aynı uğraşı veririz.

C dili grafik arabirim (görsel programlama) için pek yeterli olmadığı için pek seçenek olarak sayılmayabilir. Ama C++ olabilir. Geri kalan kısmı *python3* ile geliştireceğimizi varsayarak yapıyorum.

## Kullanılacak Teknoloji

Geliştirme için gereken teknolojiler şu an için şöyle gözüküyor:

* __GUI (Grafik Arabirimi):__ Uygulamayı geliştireceğimiz pencereleri oluşturacağımız kütüphane.
* __Media Decoder:__ Uygulamaye verilen medya dosyalarını yürütebilmemizi sağlayacak kütüphane.
* __Veri Tabanı:__ Aslında sadece dosya işleyerek de kotarabiliriz. Çok iyi bir veritabanı kullanmamıza gerek yok. 

### Grafik Arabirimi Alternetifleri:

Python'da kullanılacbilecek GUI paketleri oladukça fazladır. 

* __PyQt:__ Güçlü ve esnek bir arayüz aracıdır. Her platformda destekler. Bu kütüphaneyi kullanırsak ayrıca bir media decoder kullanmamıza gerek yok. İçinde hemen her medyayı destekleye kendi kütüphaneleri var. Aslında C++ için yapldığı için hız konusunda oldukça iyi. Ama nesne tabanlı programlama yapmak için alttan alttan baskı uyguluyor. Kendi grafik aracı var yani kodları direkt yazmanıza gerek yok.

* __Tkinter:__ Python'un içinde hazır gelen grafik arabimi  yine her platformda destekler. Kendi GUI aracı yok. Yani kendi kodlarını kendin oluşturmak zorundasın. Yazımı diğer tüm paketlere daha daha basit. Ama kendi içinde decoder yok. Harici bir kütüphane bulmamız gerekir. 

* __WxPython:__ Windows için geliştirilmiş bir arayüz aracı. Kendi içinde media decoder var. Hız ve eğitim olarak dezavantajları var. Visual Studio ile kod yazımı azaltılabilir. Diğer sistemlerde elle yazılır.

* __GTK:__ Yine her platformda çalışabilen ama daha en verimli MAC ve Linux sistemlerinde çalışan arayüz. Kendi decoderi var. Harici Gui aracı var.

Eğer python kullanacaksak. Bunlardan birini seçmeliyiz. Hepsi aşağı yukarı aynı işi yapıyor denilebilir.

### Media Decoder Alternatifleri:

Aslında listedekinden çok daha fazla var. Ama kullanımları biraz zor. Benim oyum yukarıda medya oynatabileceğimiz bir GUI aracı seçmemiz.

* __Pyglet:__ Python'da 2 boyutlu oyun yapımını sağlayan bir kütüphanedir. Müzik çalma fonksiyonlarını kullanabiliriz.

* __PyGame:__ Yine Python'da oyun yapımı için kullanlır. Müzik çalma fonksiyonlarını kullanabiliriz.

* __VLC:__ VLC media player'in sunduğu bir kütüphanedir. Müzik ve video için geniş fonksiyonları var.

* __GStreamer:__ Video ve müzik oynatmak için kullanılan isim yapmış bir kütüphane.

### Veritabanı:

Veritabnı için basit dosyalar ya da xml teknolojisini kullanabiliriz.

## Görevler:

Kullanacaklarımızı net olarak seçtikten sonra görevleri daha iyi seçebiliriz.


<hr />

## Git komutlari:

Bash kabugunu kullananlar icin git komutlari:

### CLONE komutu:

```bash
git clone <depo linki>
```
Depo ilk kez indirilirken kullanilir. Depodaki tum dosyalari yerel dizininize kopyalar. Tum commitler dahil.

### STATUS komutu:

```bash
git status
```

Yerel deponunuzda yaptiginiz degisimleri gosterir. 

### ADD komutu:

```bash
git add <dosya adi>
```

Yerel deponuzda ismini verdiginiz dosyayi ya da dosyalari ikinci kisma gonderir. Tum dosyalari bie kerede gondermek icin 
```bash
git add .
```
komutunu kullanabilirsiniz.

### COMMIT komutu:

```bash 
git commit -m "Mesaj basligi buraya gelir.
-
- Mesajin govde kismi burada olusturulur ve
- tirnak kapanana kadar mesajiniz devam 
- eder."
```

Yaptiginiz degisikliklerden **emin oldugunuzda** degisiklikleri git'e bildirmek icin kullanilir. Bu komutla birlikte gormediginiz bir hash tagi olustururlur ve tum porje bu degisiklige geri dondurulebilir. Bu yuzden commit mesajlari oldukca onemlidir ve yapilan degisiklikler detaylica belirtilmelidir.

### LOG komutu:

```bash
git log
```

Proje uzerinde yapilan tum degisiklikleri gozlemlemeye yarar. Hash taglarini, commit mesajlarini, commiti kimin gonderdigini ve gonderme zamanini bu komutla ogrenebilirsiniz.  Cikmak icin 'q' tusuna basmalisiniz.

### DIFF komutu:

```bash
git diff
```

Yaptiginiz ancak henuz commit etmediginiz degisiklikleri detaylica gosterir. Eger iki dosya icindeki farklari gostermek istiyorsaniz iki dosya yolunu da komuta eklemelisiniz.

### PUSH komutu:

```bash
git push origin master
```

Bulundugunuz daldaki degisiklieri kayitli bir uzak sunucu adresi varsa gondermek icin kullanilir.  Bir projeyi clone komutuyla cektiyseniz, cektiginiz klasor otomatik olarak uzak sunucu adresi olarak kaydeldilir. Baska dal icin master ifadesini degistirmeniz gerekir.

### PULL komutu:

```bash
git pull origin master
```

Uzak sunucudaki degisiklikleri sizin yerel deponuza uygular. Bu sayede kodlariniz guncel kalir. Ancak sadece yazdiginiz dala degisiklik uygulanir. Varsayilan dal master dalidir. Projenin ana dalidir. Baska dala degisiklik uygulamak icin kodda master kelimesini degistirip istediginiz dali yazmaniz gerekir

### Yeni dal olusturmak ve silmek:

```bash
git checkout -b Yeni_Fikir
```

Projeye yeni bir ozellik getirmek icin ya da yaptiginiz degisikliklerden emin olamadinizda yeni bir dal olusturup o dalda calisma yapabilirsiniz. Yeni dali olusturdugunuzda master dalinin kopyasini olusturursunuz. Bu dalda yaptiginiz degisiklikler master dalini etkilemez. Bu yuzden kodlarinizi daha rahat deneyebilirsiniz. 

```bash
git branch -d Yeni_Fikir
```

Olusturdugunuz dali siler.

### Kullanilan dali degistirmek:

```bash
git checkout <DAL>
```

Mevcut dalinizi degistirmeden yaptiginiz degisiklikler master dalinda kalir.

### Mevcut dali gormek

```bash
git branch
```

Tum dallari goruntuler. Mevcut dalinizin solunda * isareti vardir.

### Dalinizi ve daldaki degisimleri uzak sunucuya gondermek

```bash
git push origin <dal>
```

Dal henuz acilmamissa acilir ve dosyalar eklenir. Aciksa dosyalar guncellenir.

### Tüm yerel değişiklik ve teslimlerinizi iptal etmek

```bash
git fetch origin
```

komutu ile uzak depodaki dosyalari geri alin ve 

```bash
git reset --hard origin/master
```
komutu ile yerel deponuzu resetleyin.
