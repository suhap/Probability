# 1. Giriş
Olasılık hakkında konuşmaya başladığımız çeyrekte (hala birinci hafta) o zamandır. Yine ilk ilkelerden inşa edeceğiz. Bu hafta başında öğrendiğimiz saymayı yoğun bir şekilde kullanacağız.

# 2 Olay Uzayı ve Örnek Uzayı

Örnek uzay, S, bir deneyin tüm olası sonuçlarının kümesidir. Örneğin:

1. Yazı/Tura atma: S = Yazı, Tura
2. İki para ile Yazı/Tura atma: S = {(T, T), (T, Y), (Y, T), (Y, Y)}
3. Zar atma: S = {1, 2, 3, 4, 5, 6}
4. Bir günde gelen e-postalar: S = {x|x ∈ Z, x ≥ 0} 
5. Bir günde sosyal medyada geçirilen süre: S = {x|x ∈ R,0 ≤ x ≤ 24}

Örnek uzayın kendisine "kesin olay", bos kümeye ise "olanaksız olay" denir. Eleman sayısı sonluysa "sonlu örnek uzayı" söz konusudur. Böyle bir S uzayında her bir olaya karsı gelen sayı pozitif ve bu sayıların toplamı 1'e esitse S ye "sonlu olasılık uzayı",  Sayıların tümünün esit olması durumunda da "eş olumlu örnek uzayı" adı verilir. Eş olumlu bir örnek uzayında bir olayın olasılığı, uygun sonuçların sayısının sonuçların sayısına oranıdır.

Örnek uzayın her alt kümesi, "olay uzayı" adını alır.  Olay Uzayı, E, anlam yüklediğimiz S'nin bir alt kümesidir. Küme notasyonunda (E ⊆ S). 


1. Yazı/Tura atma olayında sonucun tura gelmesi: E = Tura
2. İki para ile Yazı/Tura atma olayında en az birinin (≥ 1) Tura gelmesi = {(T, T), (T, Y), (Y, T)}
3. Zar atma olayında sonucun 4'den az gelmesi: E = {1, 2, 3}
4. E: gün içinde gelen postaların ilk 20 tanesi: E = {x|x ∈ Z,0 ≤ x ≤ 20} (neg. olmayan ints)
5. Boşa harcanan gün (≥ 5 YouTube saati):  E = {x|x ∈ R,5 ≤ x ≤ 24}

# 3. Olasılık

Günümüzde olasılık aşağıdaki formül kullanılarak tanımlanmaktadır.

P(E) = lim n→∞ n(E)/n

Bir deneyde n deneme yaptığınızı varsayalım. İstenen E olayı olasılığı, E ile sonuçlanan denemelerin gerçekleştirilen deneme sayısına oranıdır (deneme sayınız sonsuza yaklaştıkça sınırda). Bir olasılık kavramını başka anlambilim de uygulayabilirsiniz. Atfedilen yaygın bir anlam, P (E) 'nin E'nin oluşma şansının bir ölçüsü olmasıdır.

Olasılığın başka bir anlatımı: Dünya hakkında her şeyi bilinemez. Dolayısıyla olasılık, sınırlı bilgi göz önüne alındığında, E'nin gerçekleşeceğine olan inancı ifade etmenin bir yoludur. Bu yorum, iki olasılık kaynağı olduğunu kabul eder: doğal rastgelelik ve kendi belirsizliğimiz.

Olasılığın farklı yorumları, vahşi (ve o kadar da vahşi olmayan) dünyada karşılaşacağınız olasılıkların birçok kökenine yansır. Bazı olasılıklar matematiksel kanıtlar kullanılarak analitik olarak hesaplanır. Bazı olasılıklar verilerden, deneylerden veya simülasyonlardan hesaplanır. Bazı olasılıklar sadece bir inancı temsil etmek için uydurulmuştur.

Çoğu olasılık, yukarıdakilerin bir kombinasyonundan üretilir: birisi önceden bir inanç oluşturacaktır, bu inanç veri ve kanıt kullanılarak matematiksel olarak güncellenecektir.

# 4. Olasılık Aksiyonları
Aksiyom olarak kabul ettiğimiz olasılıklarla ilgili bazı temel gerçekler şunlardır:

Temel Gerçek 1: 0 ≤ P(E) ≤ 1
Bir deneyin denemelerini gerçekleştirirken, denemelerden daha fazla olay elde etmek mümkün değildir (bu nedenle olasılıklar 1'den azdır) aynı zamanda olayın 0'dan az tekrarını elde etmek mümkün değildir.

Temel Gerçek 2: P(S) = 1
İkinci aksiyom da mantıklıdır. Olay uzaylar örnek uzayı olusturdugu kabul edilirse, herbir deneme olayı olusturacaktır. Bu durum asagıdaki gibi anlatılabilir; Pasta yerseniz (olay uzay) pasta yeme olasılıgı (örnek uzayı) 1'dir.

Temel Gerçek 3: P(E) = 1−P(E^C)
Üçüncü kural oldukça kullanıslıdır. Herhangi bir olay için, herhangi bir eleman ya olaya aittir yada degildir. Bu durumun dünyada oldukça güzel uygulamaları mevcuttur. Akşam yemeginiz ya patetesdir yada patates degildir. 


Bu bölümün geri kalanı size, X'in bir olay olduğu “X'in olasılığı nedir” şeklindeki soruları yanıtlamanız için araçlar verecektir. Örnek uzayda eşit olasılığa sahip olaylar olduğunda, veri veya simülasyon kullanarak veya diğer bilinen olasılıklardan analitik olarak bu tür soruları cevaplayabilmelisiniz. 

Bazı örnek uzayların aynı derecede olası sonuçları vardır. Bu örnek uzayları seviyoruz, çünkü bu örnek uzaylarla ilgili olasılık sorularını basitçe sayarak hesaplamanın bir yolu var. İşte eşit derecede olası sonuçların olduğu birkaç örnek:

# 5 Eşit Şanslı olaylar
Bazı örnek uzayların eşit olası sonuçları vardır. Bu örnek uzayları seviyoruz çünkü bu örnek uzaylarla ilgili olasılık sorularını basitçe sayarak hesaplamanın bir yolu var. Eşit derecede olası sonuçların olduğu birkaç örnek:

1. Yazı/Tura atma olayı: S = {Yazı, Tura}

2. İki para ile Yazı/Tura atma olayı: S = {(T, T), (T, Y), (Y, T), (Y, Y)}

3. Zar atma olayı: S = {1, 2, 3, 4, 5, 6}

Her sonuç eşit olasılığa sahip olduğundan ve örnek uzayın olasılığı 1 olması gerektiğinden, her sonucun olasılığa sahip olması gerektiğini kanıtlayabiliriz:

P(bir sonuç) = 1/|S|

Bir olay, eşit derecede olası sonuçlara sahip bir örnek uzayın bir alt kümesiyse.

Eşit Olasılıklı Sonuçların Olasılığı S, S'deki sonuçların bir alt kümesi olan bir E olayı için eşit olası sonuçlara sahip bir örnek uzay ise:

P(E) = E'deki sonuç sayısı S'deki sonuç sayısı = |E| / |S|

Eşit derecede olası sonuç kuralına dayalı bir olasılığı hesaplamak için bazı yaklaşımlar mevcuttur:
1-) Örnek uzay açıkça tanımlanması gerekmektedir. Örnek uzay içindeki tüm sonuçların esit sanslı olaylar olmalıdır. 
2-) İkinci adımda örnek uzaydaki eleman sayısı bilinmesi gerekmektedir. 
3-) Olayların sayılarının bilinmesi gerekmektedir. Olay kümesi 1. adımda tanımlanan Örnek uzayın elemanları içinden olusmalıdır. 

### örnek 1

İki zarın toplamının 7 olma olasılığı kaçtır?

Hata: Örnek alanınızı, iki zarın (2'den 12'ye kadar) tüm olası toplam değerleri olarak tanımlayabilirsiniz. Ancak bu örnek uzay "eşit olasılıklı" testte başarısız olur. Toplam 7'ye sahip olma olasılığı ile, toplam 2'ye sahip olma olasılığınız eşit değildir.

Çözüm: İki zar atıldığında olası sonuçları yazalım ve bu sonuçlarda (1,2) ile (2,1) sonuçlarının ayrı olduğuna dikkat edin. 1/36 olarak sayma çarpım kuralını kullanarak her sonucun olasılığını hesaplayabiliriz. Örnek uzaydaki tüm sonuçlar eşit derecede olasıdır:

(1, 1) (1, 2) (1, 3) (1, 4) (1, 5) (1, 6)
(2, 1) (2, 2) (2, 3) (2, 4) (2, 5) (2, 6)
(3, 1) (3, 2) (3, 3) (3, 4) (3, 5) (3, 6)
(4, 1) (4, 2) (4, 3) (4, 4) (4, 5) (4, 6)
(5, 1) (5, 2) (5, 3) (5, 4) (5, 5) (5, 6)
(6, 1) (6, 2) (6, 3) (6, 4) (6, 5) (6, 6)

Olay uzayı (iki zarın toplamının 7 olduğu örnek boşluğunun alt kümesi) kırmızıyla vurgulanır.
P(İki zarın toplamı 7) = |E| / |S| = 6/36 = 1/6
Bu teori aynı zamanda sürekli örnek uzaylar için de geçerlidir. Tüm gerçek değerli sayıların eşit olasılıkla olduğu, 0 ile 1 arasında gerçek değerli bir sayı üreten "rastgele" bilgisayar işlevinin tüm sonuçlarının örnek uzayını düşünün. Şimdi E olayını, üretilen sayının [0.3 ila 0.7] aralığında olduğunu düşünün. Örnek uzay eşit olasılığa sahip olduğundan, P(E), E'nin boyutunun S'nin boyutuna oranıdır. Bu durumda P(E) = 0.4.

# Olasılık ve Bilgisayar

Hesaplama gücündeki artış ve dijital verilerin bolluğu, birçok olasılığın bilgisayarlar tarafından ya simülasyonlar yoluyla ya da veri kümelerine sayma yoluyla hesaplandığı anlamına gelir. 

### Veriler kullanılarak Olasılık Hesaplamaları

Makine Öğrenimi (bazen Veri Bilimi olarak adlandırılır) olasılık, veri ve bilgisayarların aşk çocuğudur. Bazen makine öğrenimi karmaşık algoritmalar içerir. Ancak genellikle büyük veri kümelerine uygulanan temel olasılık fikirlerinden ibarettir.

Örnek olarak, iyi düşünülmüş makine öğrenimi sayesinde başarılı olan bir şirket olan Netflix'i ele alalım. Hesapladıkları birincil olasılıklardan biri, bir kullanıcının belirli bir filmi izleme olasılığıdır.

Rastgele bir kullanıcının, kullanıcı hakkında başka hiçbir bilgi verilmeden belirli bir filmi izlemesi olayı E olsun. Netflixteki kullanıcı sayısı çok fazla olduğu için “Kullanıcı sayısını” örnek uzay olarak kullanabiliriz. Netflix veritabanındaki kullanıcı sayısı büyük olduğundan, olasılık tanımını kullanarak P (E) 'yi yaklaşık olarak hesaplayabiliriz, bu da bazı basit sayımlarla ortaya çıkar:

P(E) = limn→∞ n(E) / n ≈ filmi izleyen kullanıcı sayısı / kullanıcı sayısı

Önemli bir uyarı olarak: Bu, yalnızca olasılığınızı hesapladığınız verilere göre bir sonuç çıkarmanıza izin verir. Örneğin, veri kümenizde Uganda'dan kullanıcılar eksikse, Uganda'da olmayan netflix kullanıcılarının filmi izleme olasılığını hesaplıyorsunuz (örneğin, dünyada rastgele bir kişinin filmi izlemiştir). Eksik verilerle başa çıkmanın zarif yolları var ve bunları daha sonra okumak için bırakıyoruz.

## Benzetimler

Olasılıkları hesaplamanın başka bir yolu da simülasyondur. Olasılıkların analitik olarak hesaplanmasının çok zor olduğu bazı karmaşık problemler için (örneğin, karmaşık kısıtlamalar olduğu için), bilgisayarlarınızın rasgele sayı üretecini kullanarak simülasyonlar çalıştırabilirsiniz.

Simülasyonlarınız örnek uzaydan rastgele örnekler üretiyorsa, bir E olayının olasılığı yaklaşık olarak E'den bir sonuç üreten simülasyonların kesrine eşittir. Yine, olasılık tanımına göre, simülasyon sayınız sonsuza yaklaştıkça, tahmin daha doğru olur.

Bu güçlü bir araç olsa da, bazen bir simülasyonun olayı tatmin edecek kadar örnek oluşturması çok uzun sürebilir. Sonuç olarak, birçok olasılık programı ilk önce bir bilgisayar bilimcisinin olasılık teorisini kullanarak olasılıkları hesaplamasıyla başlar.

# 7. VEYA (OR) olaylarının olasılığı

P(A∪B) şeklinde yazılan A olayının veya B olayının olma olasılığını nasıl hesapladığınız, gerçekten sonuç uzaylarının boyutunu saymaya benzer. İki olayın "veya" olasılığını hesaplamak için kullanabileceğiniz denklem bu olayların "birbirini engelleyen" olup olmamasına bağlıdır.

### Birbirni engelleyen olaylar

Her iki olay uzayında da hiçbir sonuç yoksa, iki olay (E ve F) birbirini dışlayan (E ∩F = ∅) olarak kabul edilir (tüm olayın, örnek uzayın alt kümeleri olan karşılık gelen bir olay uzayına sahip olduğunu hatırlayın) . İngilizce'de birbirini dışlayan, iki olayın her ikisinin birden olamayacağı anlamına gelir.

Karşılıklı dışlama görselleştirilebilir. Her sonucun bir altıgen olduğu aşağıdaki görsel örnek alanını düşünün. Elli altıgenin tümü, tam örnek alanıdır: 

![menu](https://raw.githubusercontent.com/suhap/Probability/master/resource/2-1.png)
Şekil 1. Birbirini dışalayan olaylar

Her iki olay E ve F, aynı örnek uzayının alt kümeleri olan olay uzaylarına sahiptir. Görsel olarak, iki setin çakışmadığını not edebiliriz. Birbirlerini dışlarlar: Her iki kümede de sonuç yoktur. 

### Birbirini Dışlayan Olayların Olasılığı

İki olay, E ve F birbirini dışlarsa, o zaman

P(E ∪F) = P(E) +P(F)


Bu özellik, E ve F'nin eşit olasılıklı bir örnek uzaydan olup olmadığına bakılmaksızın geçerlidir. Ayrıca, fikir ikiden fazla olayı kapsar. Diyelim ki X1,X2 ...Xn olayları var, burada her olay birbirini dışlıyor. O zamanlar:

P(X1 ∪X2 ∪··· ∪Xn) = n ∑i=1 P(Xi)

İki olayın birbirini dışlayan ise, bu olayların kesişme olasılığını ("veya") hesaplamak gerçekten basittir. Şekil 1'deki örnekte, örnek uzaydaki sonuçların eşit derecede olası olduğunu düşünürsek, E olayının 7 sonucu olduğundan P(E) = 7/50 ve F olayının 4 sonucu olduğundan P(F) = 4/50 sonuçlar. Birbirlerini dışladıkları için, şunu hesaplayabiliriz:

P(E ∪F) = P(E) +P(F) = 7 / 50 + 4 / 50 = 11 / 50 = 0.22

### Dahil etme hariç tutma

Ne yazık ki, tüm olaylar birbirini dışlamaz. E ve F olaylarının birbirini dışlamadığı durumlarda P(E ∪F) hesaplamak istiyorsanız, dahil etme hariç tutma ilkesini kullanarak çift sayımınızı hesaba katmanız gerekir:

Dahil Etme Hariç Tutma İlkesi

Herhangi iki olay için, E ve F:
P(E ∪F) = P(E) +P(F)−P(E ∩F)
Bu özellik, E ve F'nin eşit olasılıklı bir örnek uzaydan olup olmadığına ve olayların birbirini dışlayan olup olmadığına bakılmaksızın geçerlidir. Dahil Etme-Dışlama ilkesi ikiden fazla olayı kapsar, ancak önemli ölçüde daha karmaşık hale gelir. E1,E2 ...En olayları için:

P(E1 ∪E2 ∪··· ∪En) =n∑r=1 (−1)^r+1 Yr

Yr, alt kümenin boyutunun r olduğu tüm olay alt kümeleri için birleşme olasılığının toplamıdır. Bu yaklaşım genişletilirse: olayların her birinin tüm olasılıklarını kendi başlarına ekleyin. Ardından, iki olayın tüm kombinasyonlarının birleşiminin (“ve”) olasılığını çıkarın. Daha sonra, her seferinde toplamadan çıkarmaya değiştirerek, n'ye kadar tüm güç kümesi boyutları için üç olayın tüm kombinasyonlarının birleşiminin olasılığını ekleyin.

Üç olay için, E, F ve G bu formül matematiksel olarak şu şekilde genişler:
P(E ∪F ∪G) = +P(E) +P(F) +P(G) −P(E ∩F)−P(E ∩G)−P(F ∩G) +P(E ∩ F ∩G)

# 8. VE (AND) olaylarının olasılığı

E olayının ve F olayının olma olasılığını nasıl hesapladığınız, yazılı P(E ∩F) veya bazen P(EF) bunların “bağımsız” olup olmamasına bağlıdır.

### Bağımsızlık

İki olay E ve F bağımsız olarak adlandırılır, eğer: P(E ∩F) = P(E)P(F). İngilizce'de: iki olay bağımsızdır, her iki olayın olma olasılığı, her bir olayın kendi başına olma olasılığına eşittir, birlikte çarpılır. Aksi takdirde, bunlara bağımlı olaylar denir.

Bağımsızlık kavramı makine öğreniminde özellikle önemli olacaktır. Birçok olayın “ortak” olasılığını (olayların “ve” olasılığının) bilmek karmaşık sistemler için zor olabilir. Bilgisayarlar, bağımsızlık iddialarında bulunarak, temel olarak denklemin nasıl hesaplanacağını ayrıştırabilirler: Basitçe, her bir temel olayın olasılığını hesaplayarak denklemi hesaplayabilirler.

Bağımsızlık
E ve F iki olay bağımsız ise:

P(E ∩F) = P(E)P(F)

Bu özellik, E ve F'nin eşit olasılıklı bir örnek uzaydan olup olmadığına ve olayların birbirini dışlayan olup olmadığına bakılmaksızın geçerlidir. Bağımsızlık ilkesi ikiden fazla olayı kapsar. Tüm olayların birbirinden bağımsız olduğu E1,E2 ...En olayları için:

P(E1 ∩E2 ∩··· ∩En) =n ∏i=1 P(Ei)

Karşılıklı dışlama özelliğinin iki olayın OR olasılığını hesaplamayı kolaylaştırması gibi, bağımsızlık da iki olayın AND değerini hesaplamayı kolaylaştırır. İki olayın bağımsız olmadığı durumda, olasılıklarını doğrudan hesaplamanın hala yolları vardır. Ancak bunu yapmak için bir sonraki bölümde bir kavram öğrendikten sonra öğreneceğiz: Koşullu Olasılık.

Bağımsızlık matematiksel bir tanımdır ve biri size iki olayın bağımsız olduğunu söylerse, ima edilen formülü çıkarmaya hazır olmalısınız. Bunun ne anlama geldiğine dair sezgisel bir anlayış geliştirmenizi de istiyoruz. Bağımsızlık, bir olayın gerçekleşmesi diğerinin olma olasılığını etkilemediğinde ortaya çıkar. Örneğin, düzgün kenarlı bir zar (F) üzerine 4 attığınız olay, öfkeli keçiler (G) tarafından yenilme olayından bağımsızdır. Birinin olma olasılığı diğerinin olayını etkilemez ve bu nedenle her ikisinin de olma olasılığını bilmek istiyorsanız P(FG), diğerinin sonucunu dikkate almadan her olayın olasılığını hesaplayabilirsiniz.

Genellikle bağımsızlık varsayımları, tamamen doğru oldukları için değil, olasılık problemlerini çözmek için çok faydalı oldukları için yapılır. Verilerden gelen olasılıklarla çalışırken, çok az şey bağımsızlığın matematiksel tanımına uyacaktır. Bunun iki nedeni olabilir: birincisi, verilerden veya simülasyondan hesaplanan olaylar tam olarak kesin değildir. İkincisi, karmaşık dünyamızda pek çok şey, küçük bir miktar bile olsa birbirini etkiler. Buna rağmen, çoğu zaman yanlış ama faydalı bir bağımsızlık varsayımı yaparız.

# 9 Problem Çözme Stratejisi

Daha fazla olasılık aracı toplamaya geçmeden önce, duralım ve olayları içeren olasılık problemlerini çözme stratejisi hakkında konuşalım.

Olaylarınızı tanımlayın. İlk adım olarak, sorudaki tüm ilgili olaylara bir sembol verin. Ardından, bir sonraki adım olarak, çözmeye çalıştığınız soruyu bu olaylar açısından yazın.

Eşit olasılığa sahip örnek uzaylar için uyanık olun – örnek uzayın tümü eşit olasılığa sahip sonuçlara sahipse olasılıkları hesaplamak çok daha kolaydır. Bazen, sonuçların eşit derecede olası olmasını sağlamak için probleminizin altında yatan nesneleri farklı olarak düşünmek yardımcı olabilir. Örneğin, "mississippi" kelimesindeki harflerin rastgele bir permütasyonunun dört "i" nin hepsine birden sahip olma olasılığını düşünüyorsanız, harfleri farklı olarak düşünmek, farklı permütasyonlarının örnek uzaylarının hepsinin eşit derecede olası olduğu anlamına gelir. . Harfleri belirsiz olarak ele alırsanız, permütasyonlar eşit derecede olası değildir. Şaşırtıcı bir şekilde, harfleri farklı veya belirsiz olarak ele alıp almayacağınıza dair seçim size aittir. Örnek mekânları ve etkinlik alanlarını tanımlarken bu kararda tutarlı olmanız yeterlidir. Bu noktada olay çiftleri için iki özelliğimiz var: karşılıklı dışlama ve bağımsızlık. Bu özelliklere dikkat edin. Olaylar birbirini dışlıyorsa, olayların VEYA'sını hesaplamanın kolay olduğunu unutmayın. Olaylar bağımsız ise, olayların VE'sini hesaplamak kolaydır. Bazen, belirli bir olay grubunun ya bağımsız ya da birbirini dışlayan olduğunu varsayabileceğiniz size açıkça söylenecektir. Diğer zamanlarda, olduklarına dair mantıklı bir argüman yapabilirsiniz (örneğin, bir hashmap'te dizeleri karma yapıyorsanız, bir dizenin bir adreste hash işlemine tabi tutulması olayı, diğerine adreste hash işlemine tabi tutulmasıolayından karşılıklı olarak ayrıdır).

AND'leri OR'lere (ve tersi) dönüştürmek için tamamlayıcıları ve De-Morgan yasasını kullanabilirsiniz. Bu, örneğin iki olayın VEYA olasılığını hesaplamanızın istendiği ancak yalnızca bunlar arasındaki bağımsızlığı bildiğiniz durumlarda yardımcı olabilir.

Herhangi iki E ve F olayı için De Morgan Olasılık Yasası:
P((E ∩F)^C) = P(E^C ∪ F^C) Version 1
P((E ∪F)^C) = P(E^C ∩ F^C) Version 2

Bu genellikle bir olayın toplamının ve tümleyeninin 1 olduğu kuralıyla birlikte kullanılır:
P(E ∩F) = 1−P((E ∩ F)^C)     Since P(E) + P(E^C) = 1
        = 1−P(E^C ∪ F^C)     By DeMorgan’s law

P(E ∪F) = 1−P((E ∪ F)^C)     Since P(E) + P(E^C) = 1
        = 1−P(E^C ∩ B^C)     By DeMorgan’s law
