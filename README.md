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






