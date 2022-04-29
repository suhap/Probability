# Rastgele Değişkenler
Rastgele Değişken, olasılıksal olarak farklı değerler alan bir değişkendir. Bir RV'yi bir programlama dilindeki bir değişken gibi düşünebilirsiniz. Değerler alırlar, türleri vardır ve uygulanabilir oldukları alanlara sahiptirler. Rastgele değişken sayısal bir testi karşılayan bir değer alırsa meydana gelen olayları tanımlayabiliriz 
(örneğin, değişken 5'e eşit mi, değişken 8'den küçük mü). Sık sık bu tür olayların olasılıklarını düşünürüz.
Örnek olarak, üç tane adil para çevirdiğimizi varsayalım. Üç madeni paradaki toplam “tura” sayısı olarak rastgele bir Y değişkeni tanımlayabiliriz. Aşağıdaki gösterimi kullanarak Y'nin farklı değerler alma olasılığını sorabiliriz:
• P(Y = 0) = 1/8 (T, T, T)
• P(Y = 1) = 3/8 (H, T, T), (T, H, T), (T, T, H)
• P(Y = 2) = 3/8 (H, H, T), (H, T, H), (T, H, H)
• P(Y = 3) = 1/8 (H, H, H)
• P(Y ≥ 4) = 0

Rastgele değişkenler ve olaylar için aynı gösterimi kullanmamıza rağmen (her ikisi de büyük harf kullanır) bunlar farklı kavramlardır. Bir olay bir senaryodur, bir rastgele değişken bir nesnedir. Rastgele bir değişkenin belirli bir değeri (veya değer aralığını) aldığı senaryo bir olaydır. Mümkün olduğunda, olaylar için E,F,G harflerini ve rastgele değişkenler için X,Y,Z harflerini kullanmayı deneyeceğim.

Rastgele değişkenlerin kullanılması, problemlerin ayrıştırılmasına yardımcı olan uygun bir gösterim tekniğidir. Birçok farklı rasgele değişken türü vardır (gösterge, ikili, seçim, Bernoulli, vb.). Rastgele değişken türlerinin iki ana ailesi ayrık ve süreklidir. Şimdilik ayrık rastgele değişkenler etrafında sezgi geliştireceğiz.

## Olasılık Kütle Fonksiyonu PMF
Kesikli bir rasgele değişken için bilinmesi gereken en önemli şey, rasgele değişkenin alabileceği değerler ile rasgele değişkenin söz konusu değeri alma olasılığı arasındaki eşleştirmedir. Matematikte çağrışım fonksiyonları diyoruz.

Olasılık kütle fonksiyonları (PMF), rastgele bir değişkenin olası sonuçlarını karşılık gelen olasılıklarla eşleştiren bir fonksiyondur. Bu bir fonksiyon olduğu için, x ekseninin rastgele değişkenin alabileceği değerler olduğu ve y ekseninin rastgele değişkenin söz konusu değeri alma olasılığı olduğu PMF grafiklerini çizebiliriz:

![resim1](https://raw.githubusercontent.com/suhap/Probability/master/resource/4-1.png)

Şekil 1: PMF foksiyonu

Bu Olasılık Kütle Fonksiyonlarının belirtilmesinin birçok yolu vardır. Bir grafik çizebiliriz. Tüm olası olaylar için tüm olasılıkları listeleyen bir tablomuz (veya sizin için CS çalışanları için bir Harita) olabilir. Ya da matematiksel bir ifade yazabiliriz. Örneğin, iki zarın toplamı olan rastgele değişken X'i ele alalım. Olasılık kütle fonksiyonu, şeklin sağındaki grafik ile tanımlanabilir. Şu denklem kullanılarak da tanımlanabilirdi:

![formul1](https://raw.githubusercontent.com/suhap/Probability/master/resource/4f-1.png)

Olasılık kütle fonksiyonu, pX (x), X'in x değerini alma olasılığını tanımlar. Yeni pX (x) gösterimi, P(X = x) yazmak için basitçe farklı gösterimdir. Bu yeni gösterimi kullanmak, bir fonksiyon belirlediğimizi daha belirgin hale getirir. Birkaç x değeri deneyin ve pX (x) değerini şekildeki grafikle karşılaştırın. Aynı olmalılar.

## Beklenen değer
Rastgele değişken için ilgili bir istatistik, temsil ettiği deneyin birçok tekrarı üzerinden rastgele değişkenin ortalama değeridir. Bu ortalama, Beklenen Değer olarak adlandırılır.

Kesikli bir rasgele değişken X için Beklenen Değer şu şekilde tanımlanır:

![formul2](https://raw.githubusercontent.com/suhap/Probability/master/resource/4f-2.png)

Başka birçok adla gider: Ortalama, Beklenti, Ağırlıklı Ortalama, Kütle Merkezi, 1. Moment.

### örnek 1
Diyelim ki 6 Taraflı bir Zar attınız ve rastgele bir değişken X, yuvarlamanın sonucunu temsil ediyor. E[X] nedir?
Bu, ortalama değerin ne olduğunu sormakla aynıdır.

E[X] = 1(1/6) +2(1/6) +3(1/6) +4(1/6) +5(1/6) +6(1/6) = 7/2

### Örnek 2
Diyelim ki bir okulda 5, 10 ve 150 öğrenciden oluşan 3 sınıf var. Rastgele eşit olasılığa sahip bir sınıf seçersek ve X = seçilen sınıfın büyüklüğüne izin verirsek:

E[Y] = 5(1/3) +10(1/3) +150(1/3) = 165/3 = 55

Bunun yerine rasgele eşit olasılığa sahip bir öğrenci seçersek ve Y = öğrencinin bulunduğu sınıfın büyüklüğüne izin verirsek

E[X] = 5(5/165) +10(10/165) +150(150/165) = 22635/165 = 137

### Örnek 3
P = 0,5 ile tura gelen adil bir jetonla oynanan bir oyun düşünün. n = ilk "tura"dan önceki yazı tura sayısı olsun. Bu oyunda 2n kazanırsınız. Kaç dolar kazanmayı bekliyorsun? X, kazancınızı temsil eden rastgele bir değişken olsun.

![formul3](https://raw.githubusercontent.com/suhap/Probability/master/resource/4f-3.png)

### Beklenen Değerin Özellikleri

Beklentiler doğrusallığı korur, bu da şu anlama gelir:

E[aX +b] = aE[X] +b

Rastgele değişkenler eklediğiniz durumda da geçerlidir. Rastgele değişkenler arasındaki ilişkiden bağımsız olarak, toplamın beklentisi, beklentilerin toplamına eşittir. A ve B rasgele değişkenleri için:

E[A+B] = E[A] +E[B]

Bir rastgele değişken X'in g(X) fonksiyonunun beklenen değerini hesaplamak için kullanılan, X'in olasılık dağılımını bilen, ancak g'nin dağılımını açıkça bilmediği zaman, Bilinçsiz İstatistikçi Yasası adlı harika bir yasa vardır. (X).

![formul4](https://raw.githubusercontent.com/suhap/Probability/master/resource/4f-4.png)

Örneğin, rastgele bir değişkenin (ikinci an olarak adlandırılır) karesinin beklentisini hesaplamak için bilinçsiz istatistikçinin yasasını uygulayalım.

![formul5](https://raw.githubusercontent.com/suhap/Probability/master/resource/4f-5.png)
