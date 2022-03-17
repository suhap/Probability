# 1. Sayma

İlkokuldaki öğrendiğimiz sayma kavramın bu derste tekrar edilecektir. Tabiki tekrar edilecek konular olasılığın temeli olacaktır. Ayrıca ders kapsamında öngörülebilir durumlar için sayma işlemi ve farklı nesnelerin nasıl sayılacağı öğrenilecektir. Çatısı bilgisayar bilimleri(yapay zeka, makina öğrenmesi) olan olasılığın temeli ise sayma kavramıdır. 

$n^2$

# 2. Saymanın Temel İlkeleri
### Toplama kulllanılarak sayma:
Bir deneyin sonucu, m sonuç kümesinden veya n sonuç kümesinden biri olabilecekse, m sonuç kümesi ve n sonuç kümesi çakışmıyorsa yani m sonuç kümesindeki sonuçlardan herhangi biri n sonuç kümesinden herhangi biri ile aynı değilse bu deneyin olası sonuçları m+n sonuç kümesinden herhangi biridir. 
Yukarıdaki önermeyi matematiksel notasyon şeklinde yazacak olursak: 
Saymada toplama kuralı: Bir deneyin sonuç kümeleri A ve B olsun, |A|=m ve |B|=n olsun AnB = ∅  denyin muhtemel sonuç sayısı |A|+|B|=m+n olur. 


### Çarpma kullanılarak sayma:
İki olaydan birincisi n farklı şekilde, ikincisi birinci olaya bağlı olarak m farklı şekilde yapılıyor ise bu işlemler aynı anda "birinci ve ikinci" n.m şekilde yapılır. 

Küme notasyonu kullanılarak;  iki bölümden oluşan bir deneyin ilk bölümünün sonuçları A kümesinden oluşsun, burada |A| = m ve ikinci bölümünün sonuçları B kümesinden oluşsun , burada |B| = n ise, deneyin toplam çıktı sayısı |A||B| = mn

### örnek 1
Atılan hilesiz iki zarın olası kaç sonucu vardır? 

!! Atılan zarlardaki sayıların toplam değerleri yerine atışların tüm açık sonuçları ile ilgilenilmektedir.
Bu atışlar iki parça olarak düşünülebilir: ilk kısımda birinci zar atılmaktadır, ikinci kısımda ise ikinci zar atılmaktadır. İlk kısımın 6 olası değeri ve ikinci kısmın da benzer şekilde  6 olası değere sahip olabileceğinden (ilk kısımda ne geldiğinden bağımsız olarak), toplam potansiyel sonuç sayısı 36'dır (= 6 × 6). Bu olası sonuçlar bir dizi olarak aşağıda açıkça listelenmiştir:
(1, 1) (1, 2) (1, 3) (1, 4) (1, 5) (1, 6)
(2, 1) (2, 2) (2, 3) (2, 4) (2, 5) (2, 6)
(3, 1) (3, 2) (3, 3) (3, 4) (3, 5) (3, 6)
(4, 1) (4, 2) (4, 3) (4, 4) (4, 5) (4, 6)
(5, 1) (5, 2) (5, 3) (5, 4) (5, 5) (5, 6)
(6, 1) (6, 2) (6, 3) (6, 4) (6, 5) (6, 6)

### Örnek 2
İki string birbirlerinden bağımsız olarak hashing işlemine tabi tutularak 100 elemanlı bir hash tablosuna yerleştirilmek isteniyor. String ifadelerin tabloda saklanmasının kaç olası yol vardır?
Birinci string ifade hash işlemine tabi tutulduktan sonra tablodaki 100 olası adrese yerleştirilbilir. İkinci string ifade de hash işlemine tabi tutulduktan sonra diğer işlemden bağımsız olarak 100 adresten birine yerleştirilebilir. Dolayısıyla iki string ifadenin tabloda saklanmasının 100 * 100 = 10.000 yolu vardır. 

### Örnek 3
Pelin; bir kafeteryaya ait, yalnızca sıcak içecekler kısmı yırtılmış olan aşağıdaki menüyü evinde buluyor.

![menu](https://raw.githubusercontent.com/suhap/Probability/master/resource/menu.png)

Pelin bu kafeteryayı arayıp ''bir çeşit gözleme ve bir çeşit soğuk içecek'' veya ''bir çeşit poğaça ve bir çeşit sıcak içecek'' siparişi vermek istiyor. Kafeterya çalışanı bu siparişi 22 farklı şekilde verebileceğini söylüyor. Buna göre, bu kafeteryada kaç farklı sıcak içecek çeşidi vardır?

Çözüm: 

Sıcak içecek sayısı S olsun

1 gözleme + 1 soğuk içecek = 3x4 
1 poğaça + 1 sıcak içecek = 2xS

Toplam : 22 = 3x4 + 2xS  =>  S = 5


### Dahil Etme Hariç Tutma İlkesi
Bir deneyin sonucu A kümesinden veya B kümesinden alınabiliyorsa ve A ve B kümeleri potansiyel olarak çakışıyorsa (yani, A ∩ B = 0 olması garanti edilmiyorsa), bu durumda deneyin sonuç sayısı | A∪B| = |A|+|B| −|A∩B|.

A∩B = 0 olduğu durumda, Dahil Etme-Hariç Tutma İlkesi, Toplama Yoluyla Sayma Kuralı ile aynı sonucu verir.

### Örnek 3
8 bit genişliğinde bir string ifade ağ üzerinden gönderilmek istenmektedir. Verinin karşı taraftan doğru alınabilmesi için "01" bitleri ile başlamalı veya "10" bitleri ile bitmelidir. Bu şartlara uyan kaç tane string ifade mevcuttur.

Çözüm:
"10" bitleri ile başlayan 64 tane string ifade vardır. Çünkü 01 ile başladığına göre 8 bit string ifade 6 bite düşmektedir. 2^6 = 64 olasılık mevcut olacaktır. Aynı şekilde 64 tane "10" bitleri ile biten string ifade bulunmaktadır. Dikkat edilirse bu iki küme çakışmaktadır. 

2^4 =16 string ifade çakışma yaratacaktır. Küme notasyonu ile yazmak gerekirse; 
 |A| = 64, |B| = 64 ve |AnB|= 16 dolayısıyla, içerme dışlama prensibi işletilirse;
|AuB| =64+64 - 16 =112


# 3. Kombinatorik

İlk bölümdeki tanımlanan temel yapı taşları kullanılarak sayma problemlerine çözüm yaklaşımı geliştirilebilir. Bununla birlikte olasılık dünyasında oldukça yaygın olan bazı sayma problemlerini bilmek problemlere çözüm yaklaşımımızı kolaylaştıracaktır. 

## Ayrık Nesnelerin Permütasyonları

Permütasyon n farklı nesnenin sıralanmasıdır. Bu n nesne n x (n – 1) x (n – 2) x ... x 2 x 1 = n! şekilde sıralanabilir. 

Ayrık olmayan nesnelerin permütasyonu:
r tane nesne aynı ise n!/(n1!n2!...nr!)

Sayma yöntemi sıralı sayma
Üç nesneden iki tanesini seçeyim ve sıralayayım

					3	 2	= 	6
I,	II,	II				


	     II		1
I	
	    III		2


  	   I		3
II
	   III		4


     	 I		5
III
	    II		6

10 elemandan 7 tanesinin seçildiği düşünülürse:	 10	  9	  8	 7	 6	 5	 4		3,2,1 eksik
                                                 ---     ---     ---	---	---	---	---	
10!/3!		P(10,7) = 10!/3!

n elemandan r tane seçelim ve sıralayalım; n   n-1   n-2	         n-(r-1)
                                          --- ----  ---- ---  ---  ---	 -------  
                                           1    2    3                      r

                                          n-r  n-(r+1)	        3    2    1
                                          ---  -------	  ---  ---  ---	 ---    

(n-r)*(n-r+1)...2*1= (n-r)!


P(n,r)=n!/(n-r)!
						

### Örnek 4
4 haneli ekran şifresine sahip bir telefon ekrandaki rakamların üzerinde 4 tane leke(parmak izi) vardır. Kaç farklı şifre mümkündür?

Şifredeki rakamların sırası önemli olduğu için permütasyon kullanmalıyız. Dört leke olduğundan, her bir sayının farklı olduğunu bilinmektedir. Buj durumda permütasyon formülünü: 4! = 24.

Ekranda 3 rakamın üzerinde 3 leke olması durumunda kaç farklı şifre üretilebilir? 

3 rakamdan biri tekrar ediyor ama hangisi olduğu bilinmemektedir. Bu durum, tekrarlaması mümkün olan her basamak için bir tane olmak üzere (her biri aynı sayıda permütasyona sahip) üç şekilde çözülebilir. A, B bir kez C, C'nin iki kez kullanılsın. Tekrar eden C'nin farklı C'ler olduğunu varsayıldığı durumda bir önceki çözüme ulaşılır: 4! =24

A B C1 C2

Ayncak C aynı rakam olduğu için bazı durumlarda çift sayılmıştır. C'nin çift sayıldığı durumları testbit etmek için C' farklı düşündüğümüz durumlardaki C lerin kendi arasındaki permütasyonları buluruz: 2! = 4 
Bulduğumuz fazla sayımları gelen durumdan çıkarmamız gerekmekteddir. Fazla sayımlar genel durumu çarpım şeklinde etkilediği için bölme şeklinde çıkarabiliriz.  

4! /( 2!· 1!· 1!)

Yukarıdaki işlem sadece C rakamı için hesaplanmıştır. Ancak bu durum üç farklı rakam içinde aynı şekilde tekrar etmektedir. Dolayısıyla bulunan sonuç 3 ile çarpılarak olası şifrelerin sayısı bulunabilir. 

3 · 4!/(2!· 1!· 1!) = 3 · 12 = 36

Ekranda 2 rakamın üzerinde 2 leke olması durumunda kaç farklı şifre üretilebilir? 

Her biri iki kez kullanılan 2 hane veya 3 kez kullanılan 1 hane ve bir kez kullanılan diğer hane.

4!/(2!· 2!)+2 ·4!/(3!· 1!) = 6+ (2 · 4) = 6+8 = 14



### Örnek 5

BST ağacı her n düğümü için aşağıdaki üç özelliği karşılamaktadır:
1. n'nin değeri, sol alt ağacındaki tüm değerlerden büyüktür.
2. n'nin değeri, sağ alt ağacındaki tüm değerlerden küçüktür.
3. n'nin hem sol hem de sağ alt ağaçları ikili arama ağaçlarıdır.

Permütasyon formülünden 1,2,3 değerleri için 3!=6 tane ağaç mimarisi oluşturulabilmektedir. Yukarıdaki kurallar dikkate alınarak 1,2,3 değerleri yerleştirilen BST ağaçları aşağıda gösterilmektedirler. 

![BST](https://raw.githubusercontent.com/suhap/Probability/master/resource/BST.png)



## Tekrarlı Permütasyon

Ayrık Olmayan Nesnelerin Permütasyonu: Genellikle n nesne olduğunda ve

n1 aynı (ayırt edilemez) ve
n2 aynı ve
...
nr aynı ise permütasyon n! /(n1!n2!...nr!) şekilde hesaplanır. 

### Örnek 6 
Üç tane 0 ve iki tane 1'den kaç farklı bit dizisi oluşturulabilir?

5 toplam rakam 5! değerini verir. Ancak bu durum , 0'ların ve 1'lerin farklı rakamlar olduğunu varsayılmıştır:

01 11 12 02 03
01 11 12 03 02
02 11 12 01 03
02 11 12 03 01
03 11 12 01 02
03 11 12 02 01

Eğer rakamların bazıları aynı ise bu durumda bazı sıralamalar birbirinin aynı olacaktır. Dolayısıyla aynı olan sıralamalar fazladan sayılmış olacaktır. Bu durumdan kurtulmak için sıralama içinde tekrar eden nesnelerin sayısının bulunup düzeltilmesi gerekmektedir. 

Toplam = 5!/(3!·2!) = 160/( 6·2) =120/12 = 10.

## Farklı Nesnelerin Kombinasyonları

Kombinasyonlar: Bir kombinasyon, bir dizi n nesneden sırasız bir r nesne seçimidir. Tüm nesneler farklıysa, seçim yapma yollarının sayısı:
n! /(r!(n−r)!) =(n  
                 r) yol vardır.

Bu durum kısaca "n taneden r taneyi seçimi" olarak ifade edilir.

Permütasyon kullanarak kombinasyon işleminin yapılması: Bir dizi n farklı nesneden, sırasız olarak r farklı nesne seçmek istensin, 7 taneden 3 tanesi seçilsin;

1. Ölçelikle n tane nesnenin permütasyonu:  n! 
2. Bu nesneler içinden ilk r tanesi tek bir yolla seçilir.
3. Seçilen r tane nesnenin sırasızdır. Seçilen bu r nesnenin permütasyonu: r!
4. Seçilmeyen (n-r) tane nesnenin permütasyonu: (n-r)!

4. (n-r) seçilmemiş nesnelerin sırasının alakasız olduğuna dikkat edin. (n-r)! yol var. Seçim değişmeden kalır.

toplam = n! /(r!(n−r)!) = (n	= (n

                           r)   = n-r)

7 farklı nesneden 3 nesneyi seçmenin toplam yolları:

toplam = (7
              3) = 7!/(3!(7−3)!) = 35

### Örnek 7

Açlık Oyunları'nda, nüfusu 8.000 olan 12. bölgeden 2 köylü seçmenin kaç yolu vardır?

Bu basit bir kombinasyon problemidir. (8000
2) = 31.996.000.

### Örnek 8
6 kitaptan 3 kitap seçmenin kaç yolu vardır?

Kitapların her biri farklıysa, temel kombinasyon formülü :

6! /3!3!=20 yol.

Birlikte seçilmemesi gereken iki kitap varsa (örneğin, Ross ders kitabının hem 8. hem de 9. baskısını seçilemez) 3 kitap seçmenin kaç yolu vardır? Bu problemin çözümü için aşağıdaki üç farklı durumu göz önünde bulundurulması gereklidir:

Durum 1: 8. Baskı hali hazırda seçildiğinde 9. Baskı seçilemez. Dolayısıyla : 
(4
2) 

Durum 2: 9. Baskı hali hazırda seçildiğinde 8. Baskı seçilemez. Dolayısıyla :
(4
2) bunu yapmanın yolları.

Durum 3: Ne 9. Baskı ne de 8. Baskı seçilmediğinde :
(4
3) 

Saymada Toplama Kuralını kullanılarak yukarıdaki üç durum toplanabilir:
Toplam = 2 · (4  + (4
              2) + 3)   = 16

Alternatif çözüm olarak, 4 kitaptan 3 kitap seçmenin tüm yollarını hesaplanarak “yasak” istenmeyen durumlar (yani kısıtlamaya tabi olan seçimleri) çıkarılır. Chris Piech buna Yasak Şehir yöntemi denektedir.

Yasak Durum: 8. Baskı ve 9. Baskı ve diğer 1 kitabı seçilmesinin kaç yolu vardır. 
(4
1)

Toplam = Tüm olasılıklar-yasak = 20−4 = 16.


## 4 Grup Ataması

Grup atama problemleri, birçok sayma problemi için faydalı metaforlardır. Nesnelerin kaplara kaç farklı yolla doldurulabilir? Olasılık derslerinde kaplara neden çömlek denilmektedir? Jacob Bernoulli'nin oylamaya ve antik Roma'ya meraklı olamasından kaynaklanmaktadır. Antik Roma'da oy sandıkları için çömlek kullanılırdı. 

## Farklı Nesnelerin Atanması

Problem: Tüm sonuçların eşit derecede olası olduğu r adresli bir hash tablosuna  n tane string ifade konulmak isteniyor. Bunu yapmanın kaç olası yolu var? Cevap: Bunu, her birinin r sonucu olan n bağımsız deney olarak düşünebilirsiniz. Saymada çarpma kuralı: r^n

## Belirsiz Nesnelerin Atanması

Bölücü Yöntemi:

Ayırıcı problem, n tane ayırt edilemez nesne r konteynere yerleştirmek istenilmektedir. Bu problem n tane nesne ve (r–1) bölücüyü sıralanarak çözülebilir. Böylece, aynı n tane nesne ve r–1 tane bölücü toplamda n + r–1 nesnenin sıralanması problemi ortaya çıkar. 

Toplam yol = (n+r -1)! / (n!(r −1)!) =
(n+r -1
r -1)

Örnek 9
4 farklı sirkete toplamda 10 bin dolar yatırım kaç farklı sekilde yapılabilir?

Bu problem, 4 çömleğe 10 top koyma problemi ile aynıdır. Bölücü Yöntemini kullanarak:

Toplam yollar =
(10+4−1
10) =
(13
10) = 286.


3 bin dolarını birinci sirkete yatırmak kosulu ile 4 farklı sirkete toplamda 10 bin dolar yatırım kaç farklı sekilde yapılabilir?

Toplam yollar =
(7+4−1
7)
=
(10
7)
= 120

## 5 Bilgisayar Bilimi Vaka Çalışmaları
Sayma, bilgisayar bilimi dünyasında birkaç nedenden dolayı önemlidir. Öncelikle (1) olasılığı temel düzeyde anlamak için öncelikle saymayı (2) anlamakta fayda vardır, bilgisayarlar hızlıyken, bazı problemler o kadar çok iş gerektirmektedir ki, tamamlanması zaman açısından mantıksızdır. Saymayı kullanarak ne kadar iş yapılması gerektiğini daha iyi tahmin edilebilir (3) bazı sayma problemleri o kadar büyük ve karmaşıktır ki onları çözmek için hesaplamadan faydalanılır.

### Örnek: Evrendeki Atomlar

Google'ın şu anki araştırma direktörü Peter Norvig, evrendeki atomların sayısı ve bunun bilgisayar bilimi ile ilişkisi hakkında büyük bir tartışma yaptı: Gözlemlenebilir evrendeki atomların sayısı yaklaşık 10 üzeri 80 (10^80). Bu ölçü, genellikle kanonik gerçekten büyük bir sayı olarak kullanılır. Evrende kesinlikle çok sayıda atom vardır. Önde gelen bir uzmanın dediği gibi,

"Uzay büyük. Gerçekten büyük. Ne kadar uçsuz bucaksız, akıl almaz derecede büyük olduğuna inanamayacaksınız. Demek istediğim, kimyager için çok uzun bir yol olduğunu düşünebilirsiniz, yer fıstığından uzaya giden yol" -Douglas Adams

Bu sayı genellikle bilgisayarların asla çözemeyeceği görevleri göstermek için kullanılır. Sorunlar, saymanın çarpım kuralıyla hızla böyle saçma bir boyuta büyüyebilir. Birkaç örneğe bakalım.

Bir Go tahtası, kullanıcının bir taş yerleştirebileceği 19 × 19 puana sahiptir. Noktaların her biri boş veya siyah veya beyaz taşla dolu olabilir. Çarpım sayma kuralına göre, benzersiz kart konfigürasyonlarının sayısını hesaplayabiliriz. Her tahta noktası, {Siyah, Beyaz, Taş Yok} kümesindeki üç seçenekten birine sahip olmaya karar verebileceğiniz benzersiz bir seçimdir, bu nedenle 3^(19×19) ≈ 10^172 olası tahta konumu vardır, ancak “yalnızca ” bu pozisyonların yaklaşık 10^170'i yasaldır. Bu, evrendeki atom sayısının karesi ile ilgilidir. Başka bir deyişle: her bir atom için başka bir atom evreni olsaydı, ancak o zaman evrende bir Go kartının benzersiz konfigürasyonları kadar çok atom olurdu.

## Örnek: Dijital Resim Sayısı

Go konumlarından dijital resimlere geçelim. Mümkün olan her resmi görüntülemek için bir sanat projesi var. Elbette bu uzun zaman alacaktı, çünkü pek çok olası resim olmalı. Ama kaç tane? Her pikselin 2^24 ≈ 17 milyon farklı renkten biri olabileceği True Color olarak bilinen renk modelini varsayacağız.

(a) 12 milyon pikselli bir dijital kameradan, (b) 300 pikselli bir ızgaradan ve (c) sadece 12 pikselli bir ızgaradan kaç farklı resim oluşturabilirsiniz?

Resim

Cevap: Bir n piksel dizisi (17 milyon)n farklı resim üretir. (17 milyon)12 ≈ 10^86, yani küçücük 12 piksel ızgara, evrendeki atom sayısından bir milyon kat daha fazla resim üretir! 300 piksel dizisine ne dersiniz? 102167 resim üretebilir. Evrendeki atom sayısının büyük olduğunu düşünebilirsiniz, ancak bu sadece 300 piksellik bir dizideki resimlerin sayısı kadardır. Ve 12M piksel? 10^86696638 resim.

Yani olası resimlerin sayısı gerçekten, gerçekten, gerçekten çok büyük. Ve evrendeki atomların sayısı, en azından bir dizi kombinasyon olarak, nispeten küçük görünüyor. Buradaki can alıcı fikir, bir dizi fiziksel şey olarak 10^80'in gerçekten büyük bir sayı olduğudur. Ancak bir dizi şey kombinasyonu olarak 10^80 oldukça küçük bir sayıdır. 10^80'e kadar kombinasyon elde etmek için bir evren kadar malzeme gerekmez.

## Örnek: Üstel Büyümeden Yararlanma

Yukarıdaki argüman, saymanın çarpım kuralının bir sonucu olarak bazı problemlerin inanılmaz derecede zor olduğunu hissetmenize neden olabilir. Bir dakikanızı ayırıp, sayım çarpım kuralının nasıl yardımcı olabileceğinden bahsedelim! Çoğu logritmik zaman algoritması bu ilkeden yararlanır. 2^n inanılmaz derecede hızlı büyürse, log2(n)'nin muazzam n için bile küçük kalacağını da kabul eder.

Gerçek bir dünya örneği için: yakın zamanda bir meslektaşım ve ben çok fazla veri gerektiren bir makine öğrenimi projesi yapıyorduk. Aslında programlama öğrencilerine giriş için verilen bir ödev için yaklaşık 10 milyon benzersiz çözüme ihtiyacımız vardı (ki bizde yoktu). Meslektaşım ve ben verileri kendimiz oluşturmaya karar verdik. Bir programlama sorununa 10 milyon benzersiz yanıtı nasıl oluşturabiliriz? Kolaydı! Ödev için değerlendirme listesi, öğrencilerin çözümlerini yazarken alabilecekleri 24 ikili kararı ifade etti. 24 karar noktasının tamamını kodladık ve 2^24 ≈ 1,6 milyon benzersiz çözüm elde ettik!


## Örnek: Kümeleme

Bilgisayar bilimcisi olarak tüm kariyerinizin bir noktasında, muhtemelen şu satırlar boyunca bir şeyler yapmak isteyeceksiniz: verilen n nesne, her nesne çifti arasında karşılaştırma yapan bir algoritma çalıştırın. Bunun somut bir örneği, hücrelerin DNA'sına dayalı olarak tek bir kişinin vücudundan n kanser hücresinin kümelenmesinden gelir. İlk adım olarak, her hücrenin DNA'sının diğerine ne kadar benzer olduğunu hesaplamak için bir "benzerlik" metriği çalıştırmamız gerekiyor. İkili karşılaştırmayı kaç kez çalıştırmanız gerekiyor?

En basit cevap, ilk tercihin ikinciden farklı olduğu bir n kümesinden iki nesne seçmeyi düşünebilirsiniz. Böylece n×n = n^2 karşılaştırma vardır. Ama ya sıralamayı önemli görmezsek? Başka bir deyişle, A'nın B'ye benzerliği, B'nin A'ya benzerliğine eşitse, her ikisini de hesaplamamız gerekmez. Çift sayımı düzeltmek için n^ 2'yi ikiye bölmek cazip gelebilir, ancak bu düşüncede küçük bir gözden kaçma var. 14 benzersiz tür ile aşağıdaki somut örneği düşünün. Bir türün kendisiyle karşılaştırmasını dahil etmezseniz, sıranın önemli olmadığı benzersiz ikili karşılaştırmaların sayısı, 14^2 karşılaştırmanın tümünün ızgarasından sayılabilir: 91 tane vardır. Eğer orada kendileriyle karşılaştırma öğelerini eklerseniz 105 ikili karşılaştırmadır. Ne yazık ki 14^2/2 = 98. Gözden kaçan şey, öğelerin kendileriyle karşılaştırmaları dışında her karşılaştırmayı iki kez saymamızdı.

Bu soruna yaklaşmanın başka bir yolu, benzersiz karşılaştırmaların sayısını sırasız bir seçim olarak düşünerek başlamaktır. Sıranın önemli olmadığı durumlarda n'den iki öğeyi kaç farklı şekilde seçebileceğinize dair bir kuralımız var. bu basitçe
(n
2). Bu durumda
(14
2) = 91, bu doğru cevap


Kombinasyon formülünü uygularsanız, iki öğeyi değiştirmeden seçmenin birçok yolunu elde edersiniz! Başka bir deyişle, elemanların kendileriyle karşılaştırmalarını içermez. Bu tür karşılaştırmaları dahil etmek istersek, o zaman
(n
2) +n = (14
              2) +14 = 105 benzersiz karşılaştırma. 

