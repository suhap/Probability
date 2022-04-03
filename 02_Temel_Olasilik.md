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

