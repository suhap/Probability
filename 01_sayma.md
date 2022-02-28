# 1. Sayma

İlkokuldaki öğrendiğimiz sayma kavramını derslerimiz başlamadan tekrar edilecektir. Tabiki tekrar edilecek konular olasılığın temeli olacaktır. Bu bölümde öngörülebilir durumlar için sayma işlemini ve farklı nesneleri nasıl sayılacağını öğrenelicektir. Çatısı makine öğrenmesi gibi bilgisayar bilimleri olan olasılığın temeli ise sayma kavramıdır. 

# 2. Saymanın Temel İlkeleri
### Toplama kulllanılarak sayma:
Bir deneyin sonucu, m sonuç kümesinden veya n sonuç kümesinden biri olabilecekse, m sonuç kümesi ve n sonuç kümesi çakışmıyorsa yani m sonuç kümesindeki sonuçlardan herhangi biri n sonuç kümesinden herhangi biri ile aynı değilse bu deneyin olası sonuçları m+n sonuç kümesinden herhangi biridir. 
Yukarıdaki önermeyi matematiksel notasyon şeklinde yazacak olursak: 
Saymada toplama kuralı: Bir deneyin sonuç kümeleri A ve B olsun, |A|=m ve |B|=n olsun AnB = ∅  denyin muhtemel sonuç sayısı |A|+|B|=m+n olur. 


### Çarpma kullanılarak sayma:
İki olaydan birincisi n farklı şekilde, ikincisi birinci olaya bağlı olarak m farklı şekilde yapılıyor ise bu işlemler aynı anda "birinci ve ikinci" n.m şekilde yapılır. 

Küme notasyonu kullanılarak;  iki bölümden oluşan bir deneyin ilk bölümünün sonuçları A kümesinden oluşsun, burada |A| = m ve ikinci bölümünün sonuçları B kümesinden oluşsun (ilk bölümün sonucundan bağımsız olarak), burada |B| = n ise, deneyin toplam çıktı sayısı |A||B| = mn

### örnek 1
Atılan hilesiz iki zarın olası kaç sonucu vardır? 

!! Burada atılan zarlardaki sayıların toplam değerleri yerine atışların tüm açık sonuçları ile ilgilenilmektedir.
Bu atışlar iki parça olarak düşünülebilir: ilk kısımda birinci zar atılmaktadır, ikinci kısımda ise ikinci zar atılmaktadır. İlk kısımın 6 olası değeri ve ikinci kısmın da benzer şekilde  6 olası değere sahip olabileceğinden (ilk kısımda ne geldiğinden bağımsız olarak), toplam potansiyel sonuç sayısı 36'dır (= 6 × 6). Bu olası sonuçlar, bir çift zar üzerinde atılan değerleri gösteren bir dizi olarak aşağıda açıkça listelenmiştir:
(1, 1) (1, 2) (1, 3) (1, 4) (1, 5) (1, 6)
(2, 1) (2, 2) (2, 3) (2, 4) (2, 5) (2, 6)
(3, 1) (3, 2) (3, 3) (3, 4) (3, 5) (3, 6)
(4, 1) (4, 2) (4, 3) (4, 4) (4, 5) (4, 6)
(5, 1) (5, 2) (5, 3) (5, 4) (5, 5) (5, 6)
(6, 1) (6, 2) (6, 3) (6, 4) (6, 5) (6, 6)

### Örnek 2
100 elemanlı bir hash tablosu olsun. İki string birbirlerinden bağımsız olarak hashing işlemine tabi tutularak tabloya yerleştirilmektedir. String ifadelerin tabloda saklanması için kaç olası yol vardır?
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
I,	II,	II			---	---


	     II		1
I	
	    III		2


  	   I		3
II
	   III		4


     	 I		5
III
	    II		6

10 elemandan 7 tanesinin seçildiği düşünülürse:	 10	  9	  8	   7	 6	 5	 4		3,2,1 eksik
                                                 --- --- ---	---	---	---	---	
10!/3!		P(10,7) = 10!/3!

n elemandan r tane seçelim ve sıralayalım; n	 n-1	  n-2		               n-(r-1)
                                          --- -----	 -----	---  ---  ---	 -------  
                                           1    2     3                       r

                                          n-r	 n-(r+1)	        3    2    1
                                          ---  -------	  ---  ---  ---	 ---    

(n-r)*(n-r+1)...2*1= (n-r)!


P(n,r)=n!/(n-r)!
						

Örnek 4
iPhone'ların 4 haneli şifreleri vardır. Diyelim ki ekranda 4 rakamın üzerinde 4 leke var. Kaç farklı şifre mümkündür?

Koddaki rakamların sırası önemli olduğu için permütasyon kullanmalıyız. Ve tam olarak dört leke olduğundan, her bir sayının farklı olduğunu biliyoruz. Böylece permütasyon formülünü ekleyebiliriz: 4! = 24.

Ekranda 3 rakamın üzerinde 3 leke varsa ne olur? 3 rakamdan biri tekrar ediyor ama hangisi olduğunu bilmiyoruz. Bunu, tekrarlanabilecek her basamak için bir tane olmak üzere (her biri aynı sayıda permütasyona sahip) üç durum yaparak çözebiliriz. A, B, C, C'nin iki kez tekrarlandığı 3 basamağı temsil etsin. Başlangıçta iki C'nin farklı olduğunu varsayabiliriz. O zaman her vakada 4 tane olacak! permütasyonlar:

A B C1 C2

Bununla birlikte, aynı rakamların (bir A, bir B ve iki C) permütasyonlarının çift sayımını ortadan kaldırmamız gerekir:

4! /( 2!· 1!· 1!)

Farklı tekrarlanan rakamlar için üç durumu toplamak, şunu verir:
3 · 4!/(2!· 1!· 1!) = 3 · 12 = 36

Ekranda 2 hanenin üzerinde 2 leke varsa ne olur? İki olasılık vardır: Her biri iki kez kullanılan 2 hane veya 3 kez kullanılan 1 hane ve bir kez kullanılan diğer hane.

4!/(2!· 2!)+2 ·4!/(3!· 1!) = 6+ (2 · 4) = 6+8 = 14



Örnek 5

Ağaçtaki her n düğümü için aşağıdaki üç özelliği karşılayan bir ikili ağaç olan ikili arama ağacının (BST) tanımını hatırlayın:
1. n'nin değeri, sol alt ağacındaki tüm değerlerden büyüktür.

2. n'nin değeri, sağ alt ağacındaki tüm değerlerden küçüktür.

3. n'nin hem sol hem de sağ alt ağaçları ikili arama ağaçlarıdır.

1, 2 ve 3 değerlerini içeren ve dejenere bir yapıya sahip (yani, BST'deki her düğümün en fazla bir çocuğu vardır) kaç olası ikili arama ağacı vardır?

BST'deki (1, 2 ve 3) üç değerin 3!'ten herhangi birine yerleştirilmiş olabileceği gerçeğini göz önünde bulundurarak başlıyoruz (=6) sıralamalar (permütasyonlar). 3!'ün her biri için BST'ye eklenirken değerlerin sıralanabileceği şekillerde, ortaya çıkan yapının ne olacağını ve hangilerinin dejenere olduğunu belirleyebiliriz. Aşağıda, üç değerin olası her sıralamasını ve elde edilen BST yapısını ele alıyoruz.

BST Şekili


Burada 4 dejenere BST olduğunu görüyoruz (ilk ikisi ve son ikisi).

Belirsiz Nesnelerin Permütasyonları

Belirsiz Nesnelerin Permütasyonu: Genellikle n nesne olduğunda ve

n1 aynıdır (ayırt edilemez) ve
n2 aynıdır ve
...
nr aynıdır, o zaman n vardır! /(n1!n2!...nr!) permütasyonları

Örnek 6
Üç 0 ve iki 1'den kaç farklı bit dizisi oluşturulabilir?

5 toplam rakam 5 verir! permütasyonlar. Ancak bu, 0'ların ve 1'lerin ayırt edilebilir olduğunu varsayar (bunu açıklığa kavuşturmak için her birine bir alt simge verelim). İşte permütasyonların bir alt kümesi.

01 11 12 02 03
01 11 12 03 02
02 11 12 01 03
02 11 12 03 01
03 11 12 01 02
03 11 12 02 01

Aynı rakamlar ayırt edilemezse, listelenen tüm permütasyonlar aynıdır. Herhangi bir permütasyon için 3 tane var! 0'ları ve 2'yi yeniden düzenlemenin yolları! 1'leri yeniden düzenlemenin yolları (ayırt edilemez dizilerle sonuçlanır). Fazla saymışız. Belirsiz nesnelerin permütasyonları için formülü kullanarak, fazla saymayı düzeltebiliriz:

Toplam = 5!/(3!·2!) = 160/( 6·2) =120/12 = 10.

Farklı Nesnelerin Kombinasyonları

Kombinasyonlar: Bir kombinasyon, bir dizi n nesneden sırasız bir r nesne seçimidir. Tüm nesneler farklıysa, seçim yapmanın yollarının sayısı:
n! /(r!(n−r)!) =(n
                          r) yollar

Bu genellikle "n r'yi seç" olarak ifade edilir.

Ürün kombinasyonları için şu genel yolu düşünün: Bir dizi n farklı nesneden r farklı, sırasız nesne seçmek için, ör. "7 3'ü seç",

1. İlk önce tüm n nesnenin permütasyonlarını düşünün. n var! bunu yapmanın yolları.

2. Ardından permütasyondaki ilk r'yi seçin. Bunu yapmanın bir yolu var.

3. r seçilen nesnelerin sırasının alakasız olduğuna dikkat edin. r var! onları değiştirmenin yolları. Seçim değişmeden kalır.

4. (n-r) seçilmemiş nesnelerin sırasının alakasız olduğuna dikkat edin. (n-r) var! onları değiştirmenin yolları. Seçim değişmeden kalır.

toplam = n! /(r!(n−r))! = (n
                                       r) =
                                      (n
                                        n-r)

7 farklı nesneden 3 nesneyi seçmenin toplam yolları:

toplam = (7
              3) = 7!/(3!(7−3))! = 35

Örnek 7

Açlık Oyunları'nda, nüfusu 8.000 olan 12. bölgeden 2 köylü seçmenin kaç yolu vardır?

Bu basit bir kombinasyon problemidir. (8000
2) = 31.996.000.

Örnek 8
6 kitaptan 3 kitap seçmenin kaç yolu vardır?

Kitapların her biri farklıysa, bu başka bir basit kombinasyon problemidir.

Var
6! /3!3!=20 yol.

İkisi birlikte seçilmemesi gereken iki kitap varsa (örneğin, Ross ders kitabının hem 8. hem de 9. baskısını seçmeyin) 3 kitap seçmenin kaç yolu vardır? Bu sorunu vakalara bölersek çözmek daha kolay olur. Aşağıdaki üç farklı durumu göz önünde bulundurun:

Durum 1: 8. Baskıyı seçin. ve 9'uncu Basım olmayan diğer 2 kişi: Var
(4
2) bunu yapmanın yolları.

Durum 2: 9. Baskıyı seçin. ve 8 olmayan diğer 2 baskı: Var
(4
2) bunu yapmanın yolları.

Durum 3: Ne 8. ne de 8. baskı olmayan kitaplardan 3'ü seçin:
(4
3) bunu yapmanın yolları.

Eski dostumuz Toplama Kuralını kullanarak, durumları ekleyebiliriz:

Toplam = 2 · (4
2) + (4
         3)= 16.

Alternatif olarak, 4'ten 3 kitap seçmenin tüm yollarını hesaplayabilir ve ardından “yasak” olanları (yani kısıtlamayı kıran seçimleri) çıkarabilirdik. Chris Piech buna Yasak Şehir yöntemi diyor.

Yasak Dava: 8. baskı ve 9. baskı ve diğer 1 kitabı seçin. Var
(4
1) bunu yapmanın yolları (4'e eşittir).

Toplam = Tüm olasılıklar-yasak = 20−4 = 16.

Aynı doğru cevabı almanın iki farklı yolu!

4 Grup Ataması

Korkunç "toplar ve kavanozlar" olasılık örneklerini muhtemelen duymuşsunuzdur. Bunlar ne hakkında? Öğeleri kaplara doldurmayı düşünebileceğimiz birçok farklı yol bunlar. İnsanların neden kaplarına çömleği dediklerini araştırdım. Jacob Bernoulli'nin oylamaya ve antik Roma'ya meraklı olduğu ortaya çıktı. Ve antik Roma'da oy sandıkları için çömleği kullandılar. Grup atama problemleri, birçok sayma problemi için faydalı metaforlardır.

Grup atamasının birçok çeşidi olduğunu unutmayın (örneğin, değiştirme ile, değiştirme olmadan).

Farklı Nesnelerin Atanması

Problem: Diyelim ki urn'lere ayırt edilebilir n tane top koymak istiyorsunuz. (hayır bekleme öyle deme). Tamam iyi. urn yok. Tüm sonuçların eşit derecede olası olduğu bir karma tablonun r kovasına n dize koyacağımızı varsayalım. Bunu yapmanın kaç olası yolu var? Cevap: Bunu, her birinin r sonucu olan n bağımsız deney olarak düşünebilirsiniz. Arkadaşımızın Ürün Kuralı'nı kullanarak bu ortaya çıkıyor

Belirsiz Nesnelerin Atanması

Bölücü Yöntemi:

Ayırıcı problem, n tane ayırt edilemez öğeyi r konteynere yerleştirmek istediğiniz problemdir. Bölücü yöntemi, bu sorunu iki tür nesneyi, n orijinal öğelerinizi ve (r–1) bölücülerini sıralayarak çözeceğinizi hayal ederek çalışır. Böylece, n'si aynı (öğeleriniz) ve r–1'i aynı (bölücüler) olan n + r–1 nesnelerine izin veriyorsunuz. Böylece:

Toplam yol = (n+r -1)! / (n!(r −1)!) =
(n+r -1
r -1)

Örnek 9
Diyelim ki bir başlangıç ​​kuluçka merkezisiniz ve 4 şirkete yatırım yapmak için 10 milyon dolarınız var (1 milyon dolarlık artışlarla). Bu parayı kaç farklı şekilde tahsis edebilirsiniz?

Bu, 4 çömleğe 10 top koymak gibidir. Bölücü Yöntemini kullanarak şunları elde ederiz:

Toplam yollar =
(10+4−1
10) =
(13
10) = 286.

Ya 10 milyon doların tamamını yatırmanız gerekmiyorsa? (Diyelim ki ekonomi sıkı ve paranızı biriktirmek isteyebilirsiniz.)

Fazladan bir şirketiniz olduğunu hayal edin: kendiniz. Şimdi 5 şirkete 10 milyon dolar yatırım yapıyorsunuz. Bu nedenle, cevap 10 topu 5 çömleğe koymakla aynıdır.

Toplam yollar =
(10+5−1
10 )
=
(14
10)
= 1001.

Ya Şirket 1'e en az 3 milyon dolar yatırım yapmak istediğinizi biliyorsanız?

Şirket 1'e 3 milyon dolar vermenin bir yolu var. Kalan parayı yatırmanın yollarının sayısı, 7 topu 4 çömleğe koymakla aynıdır.

Toplam yollar =
(7+4−1
7)
=
(10
7)
= 120

5 Bilgisayar Bilimi Vaka Çalışmaları
Sayma, bilgisayar bilimi dünyasında birkaç nedenden dolayı önemlidir. Öncelikle (1) olasılığı temel düzeyde anlamak için öncelikle saymayı (2) anlamakta fayda var, bilgisayarlar hızlıyken, bazı problemler o kadar çok iş gerektiriyor ki, tamamlanması mantıksız bir zaman alıyor. Saymayı kullanarak ne kadar iş yapmamız gerektiğini daha iyi tahmin edebiliriz (3) bazı sayma problemleri o kadar büyük ve karmaşıktır ki onları çözmek için hesaplamadan faydalanırız.

Örnek: Evrendeki Atomlar

Google'ın şu anki araştırma direktörü Peter Norvig, evrendeki atomların sayısı ve bunun bilgisayar bilimi ile ilişkisi hakkında büyük bir tartışma yaptı: Gözlemlenebilir evrendeki atomların sayısı yaklaşık 10 üzeri 80 (10^80). Bu ölçü, genellikle kanonik gerçekten büyük bir sayı olarak kullanılır. Evrende kesinlikle çok sayıda atom vardır. Önde gelen bir uzmanın dediği gibi,

"Uzay büyük. Gerçekten büyük. Ne kadar uçsuz bucaksız, akıl almaz derecede büyük olduğuna inanamayacaksınız. Demek istediğim, kimyager için çok uzun bir yol olduğunu düşünebilirsiniz, ama bu sadece uzaya giden yer fıstığı." -Douglas Adams

Bu sayı genellikle bilgisayarların asla çözemeyeceği görevleri göstermek için kullanılır. Sorunlar, saymanın çarpım kuralıyla hızla böyle saçma bir boyuta büyüyebilir. Birkaç örneğe bakalım (yine Peter sayesinde).

Bir Go tahtası, kullanıcının bir taş yerleştirebileceği 19 × 19 puana sahiptir. Noktaların her biri boş veya siyah veya beyaz taşla dolu olabilir. Çarpım sayma kuralına göre, benzersiz kart konfigürasyonlarının sayısını hesaplayabiliriz. Her tahta noktası, {Siyah, Beyaz, Taş Yok} kümesindeki üç seçenekten birine sahip olmaya karar verebileceğiniz benzersiz bir seçimdir, bu nedenle 3^(19×19) ≈ 10^172 olası tahta konumu vardır, ancak “yalnızca ” bu pozisyonların yaklaşık 10^170'i yasaldır. Bu, evrendeki atom sayısının karesi ile ilgilidir. Başka bir deyişle: her bir atom için başka bir atom evreni olsaydı, ancak o zaman evrende bir Go kartının benzersiz konfigürasyonları kadar çok atom olurdu.

Örnek: Dijital Resim Sayısı

Go konumlarından dijital resimlere geçelim. Mümkün olan her resmi görüntülemek için bir sanat projesi var. Elbette bu uzun zaman alacaktı, çünkü pek çok olası resim olmalı. Ama kaç tane? Her pikselin 2^24 ≈ 17 milyon farklı renkten biri olabileceği True Color olarak bilinen renk modelini varsayacağız.

(a) 12 milyon pikselli bir dijital kameradan, (b) 300 pikselli bir ızgaradan ve (c) sadece 12 pikselli bir ızgaradan kaç farklı resim oluşturabilirsiniz?

Resim

Cevap: Bir n piksel dizisi (17 milyon)n farklı resim üretir. (17 milyon)12 ≈ 10^86, yani küçücük 12 piksel ızgara, evrendeki atom sayısından bir milyon kat daha fazla resim üretir! 300 piksel dizisine ne dersiniz? 102167 resim üretebilir. Evrendeki atom sayısının büyük olduğunu düşünebilirsiniz, ancak bu sadece 300 piksellik bir dizideki resimlerin sayısı kadardır. Ve 12M piksel? 10^86696638 resim.

Yani olası resimlerin sayısı gerçekten, gerçekten, gerçekten çok büyük. Ve evrendeki atomların sayısı, en azından bir dizi kombinasyon olarak, nispeten küçük görünüyor. Buradaki can alıcı fikir, bir dizi fiziksel şey olarak 10^80'in gerçekten büyük bir sayı olduğudur. Ancak bir dizi şey kombinasyonu olarak 1080 oldukça küçük bir sayıdır. 10^80'e kadar kombinasyon elde etmek için bir evren kadar malzeme gerekmez.

Örnek: Üstel Büyümeden Yararlanma

Yukarıdaki argüman, saymanın çarpım kuralının bir sonucu olarak bazı problemlerin inanılmaz derecede zor olduğunu hissetmenize neden olabilir. Bir dakikanızı ayırıp, sayım çarpım kuralının nasıl yardımcı olabileceğinden bahsedelim! Çoğu logritmik zaman algoritması bu ilkeden yararlanır. 2^n inanılmaz derecede hızlı büyürse, log2(n)'nin muazzam n için bile küçük kalacağını da kabul eder.

Gerçek bir dünya örneği için: yakın zamanda bir meslektaşım ve ben çok fazla veri gerektiren bir makine öğrenimi projesi yapıyorduk. Aslında programlama öğrencilerine giriş için verilen bir ödev için yaklaşık 10 milyon benzersiz çözüme ihtiyacımız vardı (ki bizde yoktu). Meslektaşım ve ben verileri kendimiz oluşturmaya karar verdik. Bir programlama sorununa 10 milyon benzersiz yanıtı nasıl oluşturabiliriz? Kolaydı! Ödev için değerlendirme listesi, öğrencilerin çözümlerini yazarken alabilecekleri 24 ikili kararı ifade etti. 24 karar noktasının tamamını kodladık ve 2^24 ≈ 1,6 milyon benzersiz çözüm elde ettik!

2,076 / 5,000
Translation results
Örnek: Kümeleme

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

