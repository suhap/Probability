# 1. Giriş
Olasılık hakkında konuşmaya başladığımız çeyrekte (hala birinci hafta) o zamandır. Yine ilk ilkelerden inşa edeceğiz. Bu hafta başında öğrendiğimiz saymayı yoğun bir şekilde kullanacağız.

# 2 Olay Uzayı ve Örnek UzayuÖ

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

20. yüzyılda insanlar, olasılığın ne olduğunu tam olarak tanımlamanın bir yolunu buldular:

P(E) = lim n→∞ n(E)/n

İngilizce'de bu şöyledir: Diyelim ki bir deneyin n denemesini gerçekleştiriyorsunuz. İstenen bir E olayının olasılığı, E ile sonuçlanan denemelerin gerçekleştirilen denemelerin sayısına oranıdır (deneme sayınız sonsuza yaklaştıkça limitte).

Bu matematiksel olarak titizdir. Olasılık kavramına başka anlamlar da uygulayabilirsiniz. Atfedilen yaygın bir anlam, P(E)'nin, E'nin meydana gelme şansının bir ölçüsü olmasıdır.

Bir olasılığı genellikle başka bir şekilde düşünürüm: Dünya hakkında her şeyi bilmiyorum. O zaman o gider. Sonuç olarak, sınırlı bilgim göz önüne alındığında, E'nin gerçekleşeceğine olan inancımı ifade etmenin bir yolunu bulmam gerekiyor. Bu yorum, iki olasılık kaynağı olduğunu kabul eder: doğal rastgelelik ve kendi belirsizliğimiz.

Olasılığın farklı yorumları, vahşi (ve o kadar da vahşi olmayan) dünyada karşılaşacağınız olasılıkların birçok kökenine yansır. Bazı olasılıklar matematiksel kanıtlar kullanılarak analitik olarak hesaplanır. Bazı olasılıklar verilerden, deneylerden veya simülasyonlardan hesaplanır. Bazı olasılıklar sadece bir inancı temsil etmek için uydurulmuştur.

Çoğu olasılık, yukarıdakilerin bir kombinasyonundan üretilir: birisi önceden bir inanç oluşturacaktır, bu inanç veri ve kanıt kullanılarak matematiksel olarak güncellenecektir.