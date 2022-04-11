# 1. Giriş
Olasılık hakkında konuşmaya başladığımız çeyrekte (hala birinci hafta) o zamandır. Yine ilk ilkelerden inşa edeceğiz. Bu hafta başında öğrendiğimiz saymayı yoğun bir şekilde kullanacağız.

# 2 Koşullu Olasılık
İngilizce'de, koşullu bir olasılık “başka bir F olayını zaten gözlemlemiş olduğum göz önüne alındığında, bir E olayının olma şansı nedir” der. Makine öğrenimi ve olasılıkta kritik bir fikir çünkü yeni kanıtlar karşısında inançlarımızı güncellememize izin veriyor.

Bir olayın gerçekleşmesini şart koştuğun zaman, o olayın gerçekleştiği evrene giriyorsun. Matematiksel olarak, F'yi koşullandırırsanız, F yeni örnek alanınız olur. F'nin gerçekleştiği evrende, tüm olasılık kuralları hala geçerlidir!

Koşullu olasılığı hesaplamanın tanımı:
Koşullu Olasılığın Tanımı

F olayının (diğer adıyla koşullu) zaten gerçekleştiği göz önüne alındığında, E olasılığı:

P(E|F) = P(E ∩F) / P(F)

Bunun neden doğru olduğuna dair bir sezgi edinmek için görselleştirme arkadaşımıza dönelim. Yine, her biri bir altıgen olarak çizilmiş 50 eşit olası sonuca sahip bir örnek uzayın alt kümeleri olan sonuçları olan E ve F olaylarını ele alalım:

![kosul1](https://raw.githubusercontent.com/suhap/Probability/master/resource/3-1.png)
Şekil 1: Koşullu Olasılık Sezgisi

F üzerinde koşullandırma, F'nin gerçekleştiği dünyaya girdiğimiz anlamına gelir (ve eşit derecede olası 14 sonucu olan F, yeni örnek uzayımız haline gelmiştir). F olayının gerçekleştiği göz önüne alındığında, E olayının gerçekleşmesinin koşullu olasılığı, E'nin F ile tutarlı olan sonuçlarının alt kümesidir. Bu durumda, bunların E ∩F'deki üç sonuç olduğunu görsel olarak görebiliriz. Böylece elimizde:

P(E|F) = P(E ∩F) / P(F) = (3/50) / (14/50) = 3 / 14 ≈ 0.21

Görsel örnek (eşit olasılıklı sonuç boşlukları ile) sezgi kazanmak için faydalı olsa da, örnek uzayın eşit derecede olası sonuçlara sahip olup olmadığına bakılmaksızın koşullu olasılık geçerlidir!

Zincir Kuralı
Koşullu olasılığın tanımı şu şekilde yeniden yazılabilir:

P(E ∩F) = P(E|F)P(F)

buna Zincir Kuralı diyoruz. Sezgisel olarak, E ve F olaylarını gözlemleme olasılığının, F'yi gözlemlediğiniz için E'yi gözlemleme olasılığı ile çarpılan F'yi gözlemleme olasılığı olduğunu belirtir.

Zincir Kuralının genel şekli şöyledir:

P(E1 ∩E2 ∩··· ∩En) = P(E1)P(E2|E1)...P(En|E1 ...En−1)

# 3 Toplam Olasılık Yasası

Zeki bir kişi bir keresinde, şekil 1'deki gibi bir resme baktığında, E olayının iki kısımdan oluştuğunu düşünebileceğini gözlemlemişti, F'deki kısım, (E ∩F) ve "olmayan kısım". t, (E ∩F^ C). Bu doğrudur çünkü F ve F^C, birlikte tüm örnek uzayı kapsayan birbirini dışlayan sonuç kümeleridir. Daha fazla araştırmadan sonra bunun matematiksel olarak doğru olduğu kanıtlandı ve çok sevindiriciydi:

P(E) = P(E ∩F) +P(E ∩F^C )

Bu gözlem, zincir kuralıyla birleştirildiğinde özellikle yararlı olduğunu kanıtladı ve çok yararlı bir araç ortaya çıkardı, ona büyük bir isim verildi, toplam olasılık yasası.

Toplam Olasılık Yasası

Yukarıdaki gözlemimizi zincir kuralıyla birleştirirsek çok kullanışlı bir formül elde ederiz:

P(E) = P(E|F)P(F) +P(E|F^C)P(F^C)

Kuralın daha genel bir versiyonu var. Örnek uzayınızı herhangi bir sayıda birbirini dışlayan olaya bölebilirseniz: B1,B2,...Bn, örnek uzaydaki her sonuç bu olaylardan birine düşecek şekilde, o zaman:

P(E) = n∑i=1 P(E|Bi)P(Bi)

Toplam adı (sanırım), Bi'deki olayların toplam örnek uzayını oluşturması gerektiği gerçeğinden geliyor.

# 4 Bayes Teoremi

Bayes Teoremi, bilgisayar bilimcileri için olasılık konusunda en yaygın sonuçlardan biridir. Çoğu zaman bir yönde koşullu olasılığı biliriz, diyelim ki P(E|F), ancak diğer yönde koşullu olasılığı bilmek isteriz. Bayes Teoremi, birinden diğerine dönüştürmenin bir yolunu sağlar. Koşullu olasılığın tanımıyla başlayarak Bayes Teoremini türetebiliriz:

P(E|F) = P(F ∩E) / P(F)

Şimdi, Bayes Teoremi ile sonuçlanan zincir kuralını kullanarak P(F ∩E)'yi genişletebiliriz.

Bayes teoremi
Bayes Teoreminin en yaygın biçimi:

P(E|F) = P(F|E)P(E) / P(F)

Bayes Kuralı formülündeki farklı terimlerin farklı terimleri vardır. P(E|F) terimi genellikle "arka" olarak adlandırılır, P(E) terimi genellikle "önceki" olarak adlandırılır. P(F|E) terimine güncelleme denir ve P(F) genellikle normalleştirme sabiti olarak adlandırılır.

Paydanın bilinmediği durumda (başlangıçta koşullandırdığınız olayın olasılığı), Toplam Olasılık yasasını kullanarak onu genişletebilirsiniz:

P(E|F) = P(F|E)P(E) / P(F|E)P(E) +P(F|E^C)P(E^C)

Bayes Kuralı formülünü uygulamak için yaygın bir senaryo, "gözlemlenen" bir olay veriliyken "gözlemlenemeyen" bir şeyin olasılığını bilmek istediğiniz zamandır. Örneğin, bir öğrencinin anlama olasılığını bilmek istiyorsunuz.Belirli bir problemi çözerken gözlemlediğiniz göz önüne alındığında, bir kavram. Bir öğrencinin kavramı anladığına göre bir problemi çözebilme olasılığını ilk önce tahmin etmenin ve ardından Bayes Teoremini uygulamanın çok daha kolay olduğu ortaya çıktı. Sezgisel olarak, bunu kanıta dayalı bir inancı güncellemek olarak düşünebilirsiniz.

Bayes Kuralının "genişletilmiş" versiyonu (Bayes Teoremi kutusunun altında), payda P(F)'yi hemen bilmeden çalışmanıza izin verir. Bunu daha derinlemesine incelemeye değer çünkü P(F)'nin bilinmediği ve hatta bilinemediği birçok durum var.

## 4.1 Toplam Olasılık Genel Yasası ile Bayes

Bayes'in genişletilmiş versiyonu tarafından kullanılan P(F)'yi doğrudan bilmeme sorununu çözmenin yolu, toplam olasılık yasasının basit durumunu kullanmaktı. Diğer bağlamlarda, yasanın daha genel versiyonunu kullanmak isteyebilirsiniz. Örneğin, n ayrı konumdan herhangi birinde olabilecek bir telefonu izlemeye çalıştığımızı ve telefonun Bk konumunda olup olmadığı konusunda P(B1)...P(Bn) ön inançlarına sahip olduğumuzu varsayalım. Şimdi F olarak adlandırdığımız bazı kanıtlar elde ediyoruz (belirli bir baz istasyonundan belirli bir sinyal gücü gibi) ve tüm olasılıklarımızı P(Bk |F) olacak şekilde güncellememiz gerekiyor.

Telefonun Bk , P(F|Bk) konumunda olduğunu varsayarak gözlem yapma olasılığı size bir uzman tarafından verilebilecek bir şeydir. Bu durumda, belirli bir Bk konumu verilen belirli bir sinyal gücü elde etme olasılığı, baz istasyonu ile Bk konumu arasındaki mesafe tarafından belirlenecektir. Notasyonla ilgili bir not olarak, Bk için herhangi bir yere takabilirsiniz.

Telefonun tam olarak konumlardan birinde olması gerektiğini varsaydığımız için, önce Bayes Kuralını uygulayarak ve ardından 3 toplam olasılık yasasının genel versiyonunu uygulayarak F verilen Bk olayının herhangi birinin olasılığını bulabiliriz:

P(Bk|F) = P(F|Bk)P(Bk) / P(F) = P(F|Bk)P(Bk) / ∑n i=1 P(E|Bi)P(Bi)

4.2 Göreli Olasılıklı Bayes

Bir inancı güncellemek için Bayes Teoremini kullanmak istediğimiz zamanlar vardır, ancak gözlemlenen olayın olasılığını hesaplamanın bir yolu yoktur, P(F). Tüm umutlar kaybolmaz. Bu gibi durumlarda, olayların göreceli olasılığını hala hesaplayabiliriz. Örneğin, soruyu cevaplamak istediğimizi hayal edin, bir F gözlemi verildiğinde A veya B olayı daha olasıdır. Bunu matematiksel olarak P(A|F)/P(B|F)'nin büyük olup olmadığını veya olup olmadığını hesaplayarak ifade edebiliriz. 1'e eşittir. Bu terimlerin her ikisi de Bayes kullanılarak genişletilebilir ve genişletildiklerinde P(F) terimi iptal olur:

P(A|F) / P(B|F) = {P(F|A)P(A) / P(F)} /
{P(F|B)P(B) / P(F)}

Bayes teoremi iki kez uygulandı = { P(F|A)P(A) / P(F) } · {P(F) / P(F|B)P(B)}

Bölme, tersi ile çarpmadır = P(F|A)P(A)/ P(F|B)P(B)

P(F) terimleri birbirini götürür

# 5 Koşullu Paradigma

Bir olayı koşullandırdığınızda, o olayın gerçekleştiği evrene girersiniz. Bu yeni evrende tüm olasılık yasaları geçerlidir. Bu nedenle, aynı olay üzerinde tutarlı bir şekilde koşullandırdığınız sürece, öğrendiğimiz araçların her biri hala geçerlidir. Tutarlı bir şekilde bir olaya (bu durumda G) şart koştuğumuzda birkaç eski arkadaşımıza bakalım:

Kuralın Adı Orijinal Kural Koşullu Kural

Olasılık aksiyomu 0 ≤ P(E) ≤ 1
0 ≤ P(E|G) ≤ 1

Olasılık aksiyomu P(E) = 1−P(E^C)
P(E|G) = 1−P(E^C|G)

Zincir Kuralı P(E ∩F) = P(E|F)P(F)
P(E ∩F|G) = P(E|FG)P(F|G)

Bayes Teoremi P(E|F) = P(F|E)P(E) / P(F)
P(E|FG) = P(F|EG)P(E|G) / P(F|G)

Karşılıklı dışlama ve bağımsızlık gibi diğer özellikler de, bir olaya koşullandırdığımız dünyada mevcuttur (ve bu koşullar geçerli olduğunda olasılıkları hesaplama kuralları hala geçerlidir). Bununla birlikte, bir uyarı olarak, yeni bir olaya koşullanmak, iki olay arasındaki bağımsızlığı veya karşılıklı/dışlama ilişkisini değiştirebilir.

# 6 Bağımsızlık Yeniden Ziyaret Edildi

Koşullu olasılığa ilişkin yeni anlayışımız bize bağımsızlığa dair yeni bir fikir verebilir. Aynı zamanda yeni bir kavram sunar: koşullu bağımsızlık.

İlk olarak, bu sefer iki bağımsız E ve F olayı için koşullu olasılığın tanımını tekrar gözden geçirelim:

P(E|F) = P(E ∩F) / P(F)
Koşullu olasılığın tanımı =
P(E)P(F) / P(F)

E ve F bağımsız olduğundan = P(E)

P(F) terimleri birbirini götürdüğünden

Benzer şekilde P(F|E) = P(F). Bu bize sadece bağımsız olaylarla çalışırken yeni bir formül vermekle kalmaz, bağımsızlığın ne anlama geldiğini anlamak için başka bir açı verir. Eğer iki olay birbirinden bağımsız ise, bir olayın meydana geldiğini bilmek size diğer olayın gerçekleşeceğine dair ek bir bilgi vermez.

## 6.1 Koşullu Bağımsızlık

Herhangi bir olay üzerinde koşullandırma, herhangi bir olay çiftinin bağımsızlık ilişkileri üzerinde dramatik bir etkiye sahip olabilir. Daha önce bağımsız olan olaylar bağımlı hale gelebilir. Daha önce bağımlı olan olaylar bağımsız hale gelebilir.

İki olay E ve F, G verildiğinde koşullu bağımsız olarak adlandırılır, eğer

P(E ∩F|G) = P(E|G)P(F|G)

Veya eşdeğer olarak:

P(E|F,G) = P(E|G)

İki olay, koşullanma olmadan bağımlı olsalar bile koşullu olarak bağımsız olabilir.

## 6.2 Bağımsızlığı Kırmak

Uyarı: Bu noktanın CS109'un geri kalanı üzerinde büyük bir etkisi yoktur. Ama olasılık hakkında daha tam bir anlayışa sahip olmanız için bu şaşırtıcı içgörüyü aktarmak istedim. E ve F iki olayı bağımsız ise, E|G'nin artık F|G'den bağımsız olmadığı başka bir G olayının olması mümkündür.

Örnek olarak, bir kişinin sıtması (E) veya enfeksiyonu (F) varsa ateşi (G) olduğunu varsayalım. Sıtmaya (E) ve enfeksiyona (F) sahip olmanın bağımsız olduğunu varsayacağız: bir kişinin sıtması olup olmadığını bilmek bize bir enfeksiyonu olup olmadığını söylemez. Şimdi bir hasta ateşi ile hastaneye giriyor (G). Hastanın ateşi olduğuna göre sıtma olduğuna dair inancınız, P(E|G), yüksek ve ateşi olduğuna göre hastanın enfeksiyon kaptığına dair inancınız, P(F|G) yüksek. Her ikisi de ateşi açıklar.

İlginçtir ki, zamanın bu noktasında (G koşuluna bağlı olarak), hastanın ateşi olduğuna dair bilgimiz göz önüne alındığında, hastanın sıtması olduğu bilgisini edinmek, hastanın bir enfeksiyonu olduğuna dair inancınızı değiştirecektir! Sıtma, hastanın neden ateşi olduğunu açıklar ve bu nedenle alternatif açıklama daha az olası hale gelir. (Daha önce bağımsız olan) iki olay, şimdi hastanın ateşi olmasını şart koştuğumuza bağlıdır.
