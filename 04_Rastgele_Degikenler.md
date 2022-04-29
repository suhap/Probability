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



![resim1](https://raw.githubusercontent.com/suhap/Probability/master/resource/3-1.png)
Şekil 1: Koşullu Olasılık Sezgisi
