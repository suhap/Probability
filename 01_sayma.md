1. Sayma

Üç yaşında sayma kavramını oldukça iyi kavradığınızı düşünmüş olsanız da, gerçekten saymayı öğrenmek için şimdiye kadar beklemeniz gerektiği ortaya çıktı. Şimdi bu dersi aldığına sevinmedin mi?! Ama cidden, aşağıda saymayla ilgili gelecekte yararlı bulabileceğiniz bazı özellikleri sunuyoruz.

Bu bölümde sunulan fikirler olasılığın özüdür. Sayma, bir evin temeli gibidir (ev, makine öğrenimi gibi bilgisayar bilimcileri için muhtemelen daha sonra yapacağımız tüm harika şeylerdir). Evler harika. Öte yandan, temeller hemen hemen bir delikte betondur. Ama temeli olmayan bir ev yapmayın. Bu konuda bana güven. Bu bölüm, birçok öngörülebilir durum için nasıl sayılacağını ele alırken, farklı nesnelerin nasıl sayılacağını öğrenmeye özel önem veriyoruz. Bu, olasılığa geçiş yaptığımızda faydalı olacaktır.

2 Temel Yapı Taşları
ADIMLARLA Sayma

Çarpma Sayma Kuralı:
Bir deneyin iki bölümü varsa, birinci bölümün m sonuçtan biriyle sonuçlanabileceği ve ikinci bölümün, birinci bölümün sonucuna bakılmaksızın n sonuçtan biriyle sonuçlanabileceği durumda, deneyin toplam sonuç sayısı mn'dir.

Küme notasyonu kullanılarak yeniden yazılan Ürün Kuralı, iki bölümden oluşan bir deneyin ilk bölümdeki A kümesinden bir sonucu varsa, burada |A| = m ve ikinci bölümdeki B kümesinden bir sonuç (ilk bölümün sonucundan bağımsız olarak), burada |B| = n ise, deneyin toplam çıktı sayısı |A||B| = mn

örnek 1
Yüzleri 1'den 6'ya kadar olan 6 taraflı iki zar atılıyor. Deneyin kaç olası sonucu vardır?

İki zarın toplam değeriyle değil, atışların tüm açık sonuçlarıyla ilgilendiğimizi unutmayın. İki zarı atmanın genel "deneyini" iki parçalı olarak düşünün: ilk kısımda ilk kalıbı atıyoruz, ikinci kısımda ikinci kalıbı atıyoruz. İlk kalıp 6 olası değer ve ikinci kalıp benzer şekilde 6 olası değere sahip olabileceğinden (ilk kalıpta ne göründüğünden bağımsız olarak), toplam potansiyel sonuç sayısı 36'dır (= 6 × 6). Bu olası sonuçlar, bir çift zar üzerinde atılan değerleri gösteren bir dizi çift olarak aşağıda açıkça listelenmiştir:
(1, 1) (1, 2) (1, 3) (1, 4) (1, 5) (1, 6)
(2, 1) (2, 2) (2, 3) (2, 4) (2, 5) (2, 6)
(3, 1) (3, 2) (3, 3) (3, 4) (3, 5) (3, 6)
(4, 1) (4, 2) (4, 3) (4, 4) (4, 5) (4, 6)
(5, 1) (5, 2) (5, 3) (5, 4) (5, 5) (5, 6)
(6, 1) (6, 2) (6, 3) (6, 4) (6, 5) (6, 6)

Örnek 2

100 kovalı bir hash tablosu düşünün. İki isteğe bağlı dize bağımsız olarak özetlenir ve tabloya eklenir. Dizelerin tabloda saklanması için kaç olası yol vardır?

Her dize 100 kovadan birine hash edilebilir. Birinci dizgenin hash sonuçları ikincinin hash değerini etkilemediğinden, iki dizgenin hash tablosunda saklanmasının 100 * 100 = 10.000 yolu vardır.

VEYA ile sayma

Saymanın Toplam Kuralı:
Bir deneyin sonucu m sonuçtan biri veya n sonuçtan biri olabilirse, m sonuç kümesindeki sonuçların hiçbiri n sonuç kümesindeki sonuçlardan herhangi biri ile aynı değilse, o zaman m  + n deneyin olası sonuçları.

Küme notasyonu kullanılarak yeniden yazılan Toplam Kuralı, bir deneyin sonuçlarının A kümesinden veya B kümesinden alınabileceğini belirtir; burada |A| = m ve |B| = n ve A∩B = 0 ise, deneyin sonuçlarının sayısı |A|+|B| = m+n.


Dahil Etme Hariç Tutma İlkesi

Dahil Etme-Dışlama İlkesi:
Bir deneyin sonucu A kümesinden veya B kümesinden alınabiliyorsa ve A ve B kümeleri potansiyel olarak çakışıyorsa (yani, A ∩ B = 0 olması garanti edilmiyorsa), bu durumda deneyin sonuç sayısı | A∪B| = |A|+|B| −|A∩B|.

Dahil Etme-Dışlama İlkesinin rastgele A ve B kümeleri için Toplam Sayım Kuralını genelleştirdiğine dikkat edin. A∩B = 0 olduğu durumda, Dahil Etme-Hariç Tutma İlkesi Saymanın Toplam Kuralı ile aynı sonucu verir.

Örnek 3

Bir ağ üzerinden 8 bitlik bir dize (bir bayt) gönderilir. Alıcı tarafından tanınan geçerli dizi dizisi ya 01 ile başlamalı ya da 10 ile bitmelidir. Böyle kaç tane dizi var?

Alıcının kriterlerine uyan potansiyel bit dizileri ya 01 ile başlayan 64 dizi olabilir (çünkü son 6 bit belirtilmemiş, 2^6 = 64 olasılığa izin verilir) ya da 10 ile biten 64 dizi olabilir (ilk 6 bitten beri belirtilmemiş). Elbette bu iki küme örtüşür, çünkü 01 ile başlayan ve 10 ile biten dizeler her iki kümede de vardır. Bu tür 2^4 = 16 dizi vardır (çünkü ortadaki 4 bit isteğe bağlı olabilir). Bu açıklamayı karşılık gelen küme notasyonuna çevirerek, elimizde: |A| = 64, |B| = 64 ve |A∩B| = 16, dolayısıyla Dahil Etme-Dışlama İlkesine göre, belirtilen alıcının kriterleriyle eşleşen 64+64−16 = 112 dize vardır.

Çift Sayma ve Kısıtlamalar
Bazı öğeleri birden fazla saymanın birçok nedeni vardır ("çifte sayma" olarak da bilinir). Yaygın bir durum, problemde uğraşmanız gereken bir kısıtlama olmasıdır. Fazla sayarsanız, çift sayılan öğelerin sayısını çıkarmanız gerektiğini söylemeye gerek yok. Satırları boyunca bir şey yaptıysanız: her öğeyi birkaç kat sayın, o zaman doğru son yanıtı elde etmek için toplam öğe sayınızı o kata bölebilirsiniz.

3 Kombinatorik

Sayma problemlerine birinci bölümde açıklanan temel yapı taşlarından yaklaşılabilir. Bununla birlikte, olasılık dünyasında bazı sayma sorunları o kadar yaygındır ki, birkaç üst düzey sayma soyutlaması bilmeye değer. Problemleri çözerken, bu kurallı örneklerden bir analoji bulabilirseniz, ilgili kombinatorik formüllerden oluşturabilirsiniz:

Farklı Nesnelerin Permütasyonları

Permütasyon Kuralı: Bir permütasyon, n farklı nesnenin sıralı bir düzenlemesidir. Bu n nesneye n x (n – 1) x (n – 2) x ... x 2 x 1 = n'de izin verilebilir! yollar.
Bu, farklı nesnelerin bir alt kümesine izin veriyorsanız veya bazı nesneleriniz belirsizse biraz değişir. Bu davaları kısa süre içinde ele alacağız!

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
