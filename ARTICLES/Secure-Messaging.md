# Güvenli Mesajlaşma Platformu Seçme

Bu makale, güvenli bir mesajlaşma uygulaması seçerken dikkat etmeniz gereken hususları açıklamaktadır.

**Güvenli bir mesajlaşma uygulamasını tercih etmek, üçüncü tarafların özel dönüşümlerinize erişmesini önleyebilir. E2E şifreli, açık kaynaklı ve aktif olarak bakımı yapılan bir platform seçin. Kendi kendini imha eden mesajlar, kişi doğrulama, iletme gizliliği, takma adla kaydolma (telefon numarası veya e-posta yerine) ve Tor üzerinden içerik gönderen merkezi olmayan bir P2P ağı gibi gelişmiş güvenlik özellikleri savunmayı daha da güçlendirebilir.

## Dikkat Edilmesi Gerekenler

### Uçtan Uca Şifreleme
Uçtan uca şifreleme, mesajların alıcı(lar)ınıza gönderilmeden önce cihazınızda yerel olarak şifrelendiği anlamına gelir. Ne servis sağlayıcı ne de mesajlara müdahale eden herhangi bir aktör içeriğin şifresini asla çözemez. Bu, verilerinizin bir veri ihlali, kolluk kuvveti emri, sahtekar çalışan veya kötü niyetli bir aktöre karşı güvende olması açısından önemlidir. E2E şifrelemeyi isteğe bağlı bir özellik olarak sunan uygulamalardan kaçının çünkü bu, yanlışlıkla düz metin mesaj gönderilmesi olasılığını artırabilir. Bazı sağlayıcıların zayıf veya backdore'd şifreleme sunduğunu unutmayın - (genellikle [Snake Oil Encryption] (https://en.wikipedia.org/wiki/Snake_oil_(cryptography)) olarak adlandırılır), platform açık kaynak değilse, durumun böyle olup olmadığını doğrulamanın bir yolu yoktur.

### Açık Kaynak
En güvenli tasarımlar, güvenmek zorunda olmadığınız tasarımlardır. Bir uygulama açık kaynak olmadan, gerçekten güvenli olduğunu doğrulayamayız. Arka kapıları, zayıf kriptografisi veya güvenlik açıkları olabilir. Bu, tamamen açık ve herkese açık kaynak koduna sahip uygulamaların daha güvenilir olmasının bir nedenidir Ancak yanlış reklamlara aldanmayın; bir uygulamanın açık kaynak kriptografi kullanması, tamamen açık kaynak olduğu ve dolayısıyla doğrulanamayacağı anlamına gelmez. Yayınlanan kaynak kodu eksiksiz olmalı ve güvenlik tasarım sistemi kapsamlı bir şekilde belgelenmelidir.

### Kod Denetimi
Geliştiricilerin şifrelemenin yanı sıra kod kalitesi, kullanıcı deneyimi ve hizmet kullanılabilirliğine de dikkat etmeleri gerekir. Kriptografinin arkasındaki matematik kusursuz olabilir, ancak uygulamadaki küçük bir hata güvenlik açısından ciddi sonuçlara yol açabilir. Bu nedenle kod tabanı bağımsız güvenlik uzmanları tarafından düzenli olarak denetlenmeli ve rapor kamuya açık olarak yayınlanmalıdır.

### Aktif Bakım
İyi test edilmiş güvenlik güncellemelerinin zamanında yayınlanması güvenlik açısından büyük önem taşımaktadır.  Her zaman yeni hatalar, güvenlik açıkları ve sorunlar keşfedilmektedir ve yama yapılmadan bunlar bir düşman tarafından istismar edilebilir.  Bir mesajlaşma aracının güvenli olabilmesi için, genel kararlı (beta olmayan) bir sürümün mevcut olması ve güvenlik sorunlarını hızla azaltmak için güvenli otomatik güncelleme mekanizmalarının olması gerekir. Kullanıcıya hangi sürümü çalıştırdığı ve daha yeni bir sürümün mevcut olup olmadığı açık olmalıdır

### Tekrar Üretilebilir Yapılar
Çoğu uygulama önceden derlenmiş bir biçimde dağıtılır, bu da indirdiğiniz sürümün gerçek olduğunu ve açık kaynak deposundakiyle aynı olduğunu doğrulamayı çok zorlaştırır.  [İkili Şeffaflık](https://wiki.mozilla.org/Security/Binary_Transparency), üçüncü tarafların ikili dosyaların doğrudan genel kaynak kodundan oluşturulduğunu doğrulamasına olanak tanır. [Yeniden Üretilebilir Yapılar](https://reproducible-builds.org), yapının gerçek olduğunu ve arka kapı içermediğini doğrulama uygulamasıdır. Bu, önceden tanımlanmış bir derleme ortamı ve tamamen deterministik bir derleme süreci ile yapılır - belirli bir kaynak kodu kümesinin dönüştürülmesi her zaman aynı sonucu vermelidir. Kullanıcı daha sonra isterse uygulamayı kendisi oluşturabilir ve çıktının orijinal yapıyla eşleştiğini doğrulayabilir.

### Ek Özellikler
Bazı mesajlaşma platformları kullanıcılar için cazip olabilecek ek özelliklere sahiptir, ancak bu özelliklerin güvenlik hedeflerini baltalamaması çok önemlidir. Örneğin, bulut yedeklemeleri varsayılan olarak kapalı olmalıdır ve dışa aktarılan verilerin şifresi çözülecekse kullanıcı bundan haberdar edilmelidir. Güvenlik yerine özellik geliştirmeye öncelik veren platformlardan kaçının

### Meta Veri
Mesaj göndermek ve almak meta veri oluşturur ve bu birçok bilgiyi ortaya çıkarabilir: Kiminle konuşuyorsunuz, ne sıklıkla/ne kadar süreyle, ne zaman, nerede, nasıl vb. Tüm mesajlaşma platformları bunu otomatik olarak şifrelemez, bu nedenle kontrol etmek önemlidir: Ne toplanıyor, ne kadar süreyle saklanıyor, kimlerle ve hangi amaçlarla paylaşılıyor. Genel olarak, en iyi meta veri politikaları en kısa olanlardır: Herhangi bir kullanıcı meta verisi toplamıyoruz.

### Kararlılık
Uygulama kullanılabilir, satılabilir ve güvenilir olmalıdır.  En büyük tehlikelerden biri, platformun mesajları güvenilir bir şekilde iletememesi durumunda kullanıcıların daha az güvenli kanallara geri dönmek zorunda kalabilmesidir.  Bazı küçük mesajlaşma hizmetleri sağlam ve güvenilir bir mesajlaşma platformu oluşturmak için gereken kaynaklara sahip olmayabilir, ancak bu güvenlik için çok önemlidir.

### Finansman
Uygulama oluşturmak ve sunucuların bakımını yapmak pahalıdır. Kendinize sorun - tüm bunlar için kim ödeme yapıyor? Çünkü genellikle, eğer bir hizmet ücretsizse - ürün sizsinizdir. Bazı açık kaynak kodlu uygulamalar bağış ve sponsorluk alan kar amacı gütmeyen kuruluşlar tarafından finanse edildiği için bu her zaman geçerli değildir.  Ancak uygulamanın arkasında kimin olduğunu kolayca bulamıyorsanız, bu bir kırmızı bayrak olmalıdır.

### Saygın Geliştiriciler
Geliştiriciler, platformla ilgili teknik sorunlara ve yasal tehditlere yanıt verme konusunda sağlam bir geçmişe sahip olmanın yanı sıra hükümet ve kolluk kuvvetlerine karşı gerçekçi ve şeffaf bir tutum sergilemelidir


### Yargı Yetkisi 
Şirketin yasal olarak nerede kayıtlı olduğu, operasyonlarını nereden yürüttüğü ve kullanıcı verilerini nerede barındırdığı güvenlik açısından büyük rol oynar. Bazı ülkelerde veya eyaletlerde, kuruluşlar yerel hükümet düzenlemelerine uymak zorunda kalırlar, bu da genellikle kuruluşun tüm kullanıcı verilerini kaydetmesini veya herhangi bir şifreleme anahtarını teslim etmesini gerektirebilir. Genel olarak, [Beş Göz] (https://en.wikipedia.org/wiki/Five_Eyes) İttifakı dahilindeki şirketlerden kaçınmak daha iyidir.

### Anonimlik
Uygulama bir telefon numarası, e-posta adresi veya isim isterse, anonim değilsiniz demektir.  Savunmasız kullanıcılar için, telefon numarası gibi önemli bir tanımlayıcı özel bilgi olduğundan ve kimliklerini bilen biri (hükümet, takipçi veya suç düşmanı gibi) tarafından hedefleniyorlarsa riskli olabileceğinden, anonim olarak kaydolma yeteneği kritik öneme sahiptir. Bu herkes için gerekli olmayabilir, ancak hedef alınabileceğinizi düşünüyorsanız, anonim bir mesajlaşma uygulamasını tercih edin, Google Play / Apple App Store dışında Tor üzerinden indirin, anonim bir kimlik oluşturun ve uygulamayı yalnızca Tor üzerinden bağlıyken çalıştırın.

### İletişim Doğrulama
İletişimleriniz ancak en zayıf halka kadar güvenli olabilir ve kişilerinizin kimliğini doğrulayamazsanız, hesaplarının ele geçirilmediğinden ve hatta amaçlanan varlıkla iletişim kurduğunuzdan emin olamazsınız. Aynı şekilde, alıcınızın kimliği ele geçirilmişse, mesajlarınız hiç de güvenli değildir. İletişim parmak izi doğrulaması, kullanıcıların hedefe güvenmesini sağlayan ve bilgisayar korsanlarının görüşmeyi ele geçirmesini önleyen güçlü bir özelliktir. Genellikle bir telefon görüşmesi sırasında veya gerçek hayatta bir QR kodu aracılığıyla parmak izi kodlarının karşılaştırılması şeklinde gerçekleşir. Güvenli bir mesajlaşma programı, son kullanıcı tarafından tanınabilen güvenilir uzlaşma göstergeleri sağlamalıdır; bu nedenle, birisi yeni bir cihazdan oturum açtıysa, her iki taraf da bilgilendirilmelidir.

### Geçici Mesajlar
Cihazınızın fiziksel güvenliğine her zaman güvenemezsiniz. Kendi kendini imha eden mesajlar, mesajlarınızın belirli bir süre sonra otomatik olarak silinmesine neden olan gerçekten güzel bir özelliktir. Bu, cihazınız kaybolur ya da çalınırsa, bir düşmanın yalnızca en son iletişimlere erişebileceği anlamına gelir. Uzaktan silmenin aksine, mesajların kaybolması cihazınızın uzaktan erişilebilir olmasını veya sinyal almasını gerektirmez. Tehdit modelinize bağlı olarak bu zaman dilimini haftalardan sadece birkaç saniyeye kadar değiştirebilirsiniz.

### İleriye Yönelik Gizlilik
İleri gizlilik] (https://en.wikipedia.org/wiki/Forward_secrecy) uygulayan bir platform tercih edin. Bu, uygulamanızın her mesaj için yeni bir şifreleme anahtarı ürettiği yerdir, daha sonra düşmanınız cihazınızı ele geçirmiş ve özel şifreleme anahtarını çıkarmış olsa bile, daha önce ele geçirilen mesajların şifresini çözmek için kullanamazlar. Bu, bir tarafın anahtarı ele geçirilse bile, bu anahtarla oturumun geri kalanının şifresini çözmenin mümkün olmayacağı anlamına gelir.

### Merkeziyetsizlik
Özgürlük olmadan, uygulamanız tek bir hata noktasına sahip olacaktır. Tüm veriler merkezi bir sağlayıcı üzerinden akıyorsa, meta verileriniz konusunda onlara güvenmeniz gerekir. Ve eğer bu sağlayıcı çalışmayı durdurursa, tüm ağ o süre boyunca kullanılamaz hale gelecektir. Oysa merkezi olmayan bir sistemde, güveni başka bir yetki alanındaki başka birine devretme özgürlüğüne sahipsiniz. Tamamen eşler arası bir uygulamada, tehlikeye atılacak merkezi sunucular yoktur ve tek bir hata noktası yoktur.

## Ek Ayarlar
Okundu bilgisi, son çevrimiçi ve yazma bildirimi gibi isteğe bağlı güvenlik dışı özellikleri devre dışı bırakmanıza izin veren bir uygulama seçin. Uygulama, yedekleme veya bir web uygulaması arkadaşı aracılığıyla erişim için bulut senkronizasyonunu destekliyorsa, bu saldırı yüzeyini artırır ve bu nedenle de devre dışı bırakılmalıdır.

## Son Hususlar
Herhangi bir sistemdeki en zayıf nokta kullanıcıdır. Siz veya alıcınız tehlikeye girerseniz, en gelişmiş güvenlik özellikleri bile kullanılmaz hale gelecektir. İyi güvenlik uygulamalarını takip edin ve iletişim kurduğunuz kişinin de bunu yaptığından emin olun. Her zaman yeni güvenlik açıklarının keşfedildiğini ve kullanıldığını ve bugünün en güvenli mesajlaşma uygulamasının gelecekte tehlikeye girebileceğini unutmamak önemlidir

