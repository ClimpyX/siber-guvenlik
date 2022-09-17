# Kişisel Siber Güvenlik | TLDR [![Awesome](https://awesome.re/badge-flat2.svg)](https://awesome.re) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com) [![License](https://img.shields.io/badge/LICENSE-CC_BY_4.0-00a2ff?&style=flat-square)](https://creativecommons.org/licenses/by/4.0/)[![Contributors](https://img.shields.io/github/contributors/lissy93/personal-security-checklist?color=%23ffa900&style=flat-square)](/ATTRIBUTIONS.md#contributors-)

#### Contents
- [Kişisel Güvenlik Kontrol Listesi](#personal-security-checklist)
- [Gizlilik Odaklı Yazılım](#open-source-privacy-focused-software)
- [Güvenlik Donanımı](#security-hardware)

## KİŞİSEL GÜVENLİK KONTROL LİSTESİ

> Gizlilik ve güvenlik ipuçlarını içeren bu kontrol listesi, [The Complete Personal Security Checklist] (https://github.com/Lissy93/personal-security-checklist/blob/master/README.md)'in özetlenmiş bir versiyonudur. Dijital hayatınızı korumak için atmanız gereken en temel adımları ortaya koymaktadır.

### Kimlik Doğrulama
- Her bir hesabınız için uzun, güçlü ve benzersiz bir parola kullanın (bkz. [HowSecureIsMyPassword.net](https://howsecureismypassword.net))
- Kimlik bilgilerini şifrelemek, saklamak ve doldurmak için [BitWarden](https://bitwarden.com) veya [KeePass](https://keepass.info) / [KeePassXC](https://keepassxc.org) gibi güvenli bir [şifre yöneticisi](https://github.com/Lissy93/awesome-privacy#password-managers) kullanın
- Mümkün olan yerlerde 2 Faktörlü kimlik doğrulamayı etkinleştirin ve bir [kimlik doğrulayıcı uygulama](https://github.com/Lissy93/awesome-privacy#2-factor-authentication) veya [donanım belirteci](/6_Privacy_and-Security_Gadgets.md#fido-u2f-keys) kullanın
- Çok faktörlü kimlik doğrulamayı etkinleştirdiğinizde, genellikle 2FA yönteminiz kaybolursa, bozulursa veya kullanılamaz hale gelirse kullanabileceğiniz birkaç kod verilir. Bunları kağıt üzerinde veya disk üzerinde güvenli bir yerde saklamalısınız (örneğin çevrimdışı depolamada veya şifrelenmiş bir dosya / sürücüde olduğu gibi).
- İhlal uyarıları için kaydolun ([Firefox Monitor](https://monitor.firefox.com) veya [HaveIBeenPwned](https://haveibeenpwned.com) ile) ve ele geçirilen hesapların şifrelerini güncelleyin


### Tarayıcı
- Gizliliğe Saygı Gösteren Bir Tarayıcı Kullanın, [Brave](https://brave.com) ve [Firefox](https://www.mozilla.org/en-US/exp/firefox/new) iyi seçeneklerdir. Varsayılan aramanızı izleme yapmayan bir motora ayarlayın, örneğin [DuckDuckGo](https://duckduckgo.com)
- HTTPS olmayan bir web sitesine herhangi bir bilgi girmeyin (kilit simgesini arayın). Firefox, Chrome, Edge ve Safari artık entegre HTTPS güvenlik özelliklerine sahiptir; etkin olup olmadığını bilmiyorsanız, nereye bakacağınızı öğrenmek için bu [kılavuz](https://www.eff.org/deeplinks/2021/09/https-actually-everywhere)'a göz atın.
- [Privacy Badger](https://privacybadger.org) veya [uBlock](https://github.com/gorhill/uBlock) gibi bir uzantı kullanarak istilacı 3. taraf izleyicileri ve reklamları engelleyin
- Tarayıcınızı güncel tutun, gizlilik ayarlarını keşfedin ve gereksiz eklentileri/uzantıları kaldırın
- İzlemeyi azaltmak için gezintinizin farklı alanlarını (iş, sosyal, alışveriş vb.) ayırmak için bölümlere ayırmayı kullanmayı düşünün. Bu, [Firefox Containers](https://support.mozilla.org/en-US/kb/containers) ile veya ayrı tarayıcılar veya tarayıcı profilleri kullanarak yapılabilir
- Tarayıcınızın şifrelerinizi kaydetmesine veya kişisel bilgilerinizi otomatik doldurmasına izin vermeyin (bunun yerine bir [şifre yöneticisi](https://github.com/Lissy93/awesome-privacy#password-managers) kullanın ve [tarayıcınızın kendi otomatik doldurmasını devre dışı bırakın](https://www.computerhope.com/issues/ch001377.htm))
- Çerezlerinizi, oturum verilerinizi ve önbelleğinizi düzenli olarak temizleyin. Bunu otomatikleştirmek için [Cookie-Auto-Delete](https://github.com/Cookie-AutoDelete/Cookie-AutoDelete) gibi bir uzantı kullanılabilir
- Kimliğinize daha fazla veri bağlayabileceğinden tarayıcınızda oturum açmayın. İhtiyacınız varsa, açık kaynaklı bir [yer imi senkronizasyonu](https://github.com/Lissy93/awesome-privacy#browser-sync) uygulaması kullanabilirsiniz
- Cihazınızın yaptığı izlenebilir CDN isteklerinin sayısını azaltmak için [Decentraleyes](https://decentraleyes.org) kullanmayı düşünün
- Önemli bir sorun olmadığından emin olmak için [Panopticlick](https://panopticlick.eff.org) gibi bir araç kullanarak tarayıcınızı test edin. [BrowserLeaks](https://browserleaks.com) ve [Am I Unique](https://amiunique.org/fp) de web sitelerine hangi cihaz bilgilerini ifşa ettiğinizi keşfetmek için kullanışlıdır
- Anonim gezinme için [The Tor Browser](https://www.torproject.org/) kullanın ve kişisel hesaplarınızda oturum açmaktan kaçının


### Telefon
- Bir cihaz PIN kodu belirleyin, ideal olarak uzun bir parola kullanın. Destekleniyorsa, parmak izi kimlik doğrulamasını yapılandırın, ancak yüz kilidini açmaktan kaçının
- Verilerinizi fiziksel erişime karşı güvende tutmak için cihazınızı şifreleyin. Etkinleştirmek için, Android için: `Ayarlar --> Güvenlik --> Şifreleme` veya iOS için: `Ayarlar --> TouchID ve Parola --> Veri Koruma`
- Cihazı güncel tutun. Sistem güncellemeleri genellikle yakın zamanda keşfedilen güvenlik açıkları için yamalar içerir. İstendiğinde güncellemeleri yüklemelisiniz
- Uygulama izinlerini gözden geçirin. İhtiyacı olmayan uygulamalara erişim izni vermeyin. (Android için, geçici izinler vermenizi sağlayan bir uygulama olan [Bouncer](https://play.google.com/store/apps/details?id=com.samruston.permission&hl=en_US)'a da bakın)
- Kullanılmayan bağlantı özelliklerini devre dışı bırakın ve artık ihtiyaç duymadığınız WiFi ağlarını 'unutun'
- Konum izlemeyi devre dışı bırakın. Varsayılan olarak, hem Android hem de iOS GPS konum geçmişinizi kaydeder. Bunu Android için: `Haritalar --> Ayarlar --> Konum Geçmişi` ve iOS için: `Ayarlar --> Gizlilik --> Konum Servisleri --> Sistem Servisleri --> Yerler` seçeneklerinden devre dışı bırakabilirsiniz. Üçüncü taraf uygulamaların konumunuzu kaydetmeye devam edebileceğini ve konumunuzu belirlemek için GPS dışında başka yöntemler de olduğunu unutmayın (Baz istasyonu, WiFi, Bluetooth vb.)
- İhtiyaç duymaması gereken uygulamaların internet bağlantısını engellemek için bir uygulama güvenlik duvarı kullanın. [NetGuard](https://www.netguard.me/) (Android) veya [Lockdown](https://apps.apple.com/in/app/lockdown-apps/id1469783711) (iOS) gibi
- Uygulamaların verilerinizi toplayan, depolayan ve bazen paylaşan izleyiciler içerdiğini anlayın. Android için, yüklü uygulamalarınızın hangi izleyicileri kullandığını ortaya çıkarmak için [Exodus](https://exodus-privacy.eu.org/en/page/what/) kullanabilirsiniz.


### E-posta
E-posta hesabınızı korumanız önemlidir, çünkü bir bilgisayar korsanı bu hesaba erişim sağlarsa sizin gibi davranabilir ve diğer çevrimiçi hesaplarınızın şifrelerini sıfırlayabilir. Dijital güvenliğe yönelik en büyük tehditlerden biri hala kimlik avıdır ve bazen inanılmaz derecede ikna edici olabilir, bu nedenle tetikte olun ve [kötü niyetli e-postaların nasıl tespit edileceğini](https://heimdalsecurity.com/blog/abcs-detecting-preventing-phishing) anlayın ve e-posta adresinizi herkese açık olarak paylaşmaktan kaçının

- Uzun, güçlü ve benzersiz bir parola kullanın ve 2FA'yı etkinleştirin
- [ProtonMail](https://protonmail.com) veya [Tutanota](https://tutanota.com) gibi güvenli ve şifreli bir posta sağlayıcısına geçmeyi düşünün
- Gerçek posta adresinizi korumak için [Anonaddy](https://anonaddy.com) veya [SimpleLogin](https://simplelogin.io/?slref=bridsqrgvrnavso) gibi bir sağlayıcı ile e-posta takma adı kullanın. Bu, gerçek adresinizi gizli tutmanıza, ancak yine de tüm iletilerin birincil gelen kutunuza düşmesine olanak tanır
- Genellikle ayrıntılı izleme için kullanıldığından ancak kötü amaçlı da olabileceğinden, uzak içeriğin otomatik olarak yüklenmesini devre dışı bırakın
- Özel bir alan adı kullanmak, mevcut sağlayıcınızın ortadan kalkması durumunda e-posta adresinize erişiminizi kaybetmeyeceğiniz anlamına gelir. Mesajları yedeklemeniz gerekiyorsa, güvenli bir IMAP istemcisi [Thunderbird](https://www.thunderbird.net) kullanın


### Güvenli Mesajlaşma
- Hem tamamen açık kaynaklı hem de mükemmel ileri gizlilik ile uçtan uca şifrelenmiş bir [güvenli mesajlaşma uygulaması](https://github.com/Lissy93/awesome-privacy#encrypted-messaging) kullanın (örneğin [Signal](https://www.signal.org/))
- Hem kendi cihazınızın hem de alıcı(lar)ınızın cihazının güvenli olduğundan (kötü amaçlı yazılım içermediğinden, şifreli olduğundan ve güçlü bir parolaya sahip olduğundan) emin olun
- Her ikisi de saldırı yüzeyini artıran web uygulaması eşlikçisi veya bulut yedekleme özelliği gibi bulut hizmetlerini devre dışı bırakın
- Paylaşmadan önce meta verileri medyadan çıkarın, çünkü bu istemeden amaçladığınızdan daha fazla verinin açığa çıkmasına neden olabilir
- Kişi doğrulaması sunan bir uygulama kullanarak alıcınızın iddia ettiği kişi olduğunu fiziksel olarak veya kriptografik olarak doğrulayın
- SMS'ten kaçının, ancak kullanmanız gerekiyorsa mesajlarınızı şifreleyin, örneğin [Silence](https://silence.im/) uygulamasını kullanarak
- Saygın geliştiriciler tarafından desteklenen ve şeffaf bir gelir modeline sahip olan veya finansmanın nereden geldiğini açıklayabilen istikrarlı ve aktif olarak sürdürülen bir mesajlaşma platformunu tercih edin. İdeal olarak dost bir yargı bölgesinde yer almalı ve bağımsız bir güvenlik denetiminden geçmelidir. 
- Bazı durumlarda, kaybolan mesajları destekleyen ve/veya anonim kaydolmaya izin veren (herhangi bir PII olmadan: telefon numarası, e-posta adresi vb.) bir uygulama kullanmak uygun olabilir. Merkezi olmayan bir platform](https://github.com/Lissy93/awesome-privacy#p2p-messaging) bazı durumlarda ek güvenlik ve gizlilik avantajları sunabilir, çünkü onu yöneten tek bir varlık yoktur, örneğin [Matrix](https://matrix.org/), [Session](https://getsession.org/), [Tox](https://tox.chat/) veya [Briar](https://briarproject.org/)


### Ağ İletişimi
- IP'nizi korumak ve İSS'nizin kaydedebileceği tarama verilerinin miktarını azaltmak için saygın bir VPN kullanın, ancak [sınırlamalarını](5_Privacy_Respecting_Software.md#word-of-warning-4) anlayın.  İyi seçenekler arasında [ProtonVPN](https://protonvpn.com) ve [Mullvad](https://mullvad.net) bulunmaktadır, ayrıntılı karşılaştırmalar için [thatoneprivacysite.net](https://thatoneprivacysite.net/) adresine bakın
- Yönlendiricilerinizin varsayılan şifresini değiştirin. WiFi ağınıza bağlanan herkes ağ trafiğini dinleyebilir, bu nedenle tanımadığınız kişilerin bağlanmasını önlemek için WPA2 kullanın ve güçlü bir şifre belirleyin.
- İzlemeyi azaltmak için bir [güvenli DNS](https://github.com/Lissy93/awesome-privacy#dns) sağlayıcısı kullanın (örneğin [Cloudflare's 1.1.1.1](https://1.1.1.1/dns/)). İdeal olarak bunu yönlendiricinizde yapılandırın, ancak bu mümkün değilse, her cihazda yapılabilir. 


**📜 Daha Fazlasına Bakın**: [Eksiksiz Kişisel Güvenlik Kontrol Listesi](https://github.com/Lissy93/personal-security-checklist/blob/master/README.md)

----


## AÇIK KAYNAKLI, GIZLILIK ODAKLI YAZILIM
Verilerinizi toplamayan, sizi takip etmeyen veya hedefli reklamlar göstermeyen alternatif açık kaynaklı, gizliliğe saygılı uygulama ve hizmetlere geçin.

#### Güvenlik
- Parola Yöneticileri: [BitWarden] | [1Password] *(özel)* | [KeePassXC] *(çevrimdışı)* | [LessPass] *(durum bilgisi olmayan)*
- 2 Faktörlü Kimlik Doğrulama: [Aegis] *(Android)* | [Authenticator] *(iOS)* | [AndOTP] *(Android)*
- Dosya Şifreleme: [VeraCrypt] | [Cryptomator] *(bulut için)*
- Şifreli Mesajlaşma: [Signal] | [KeyBase] *(gruplar/topluluklar için)*
- Şifreli E-posta: [ProtonMail] | [MailFence] | [Tutanota] | (+ ayrıca takma ad için [33Mail] | [anonaddy])
- Özel Tarayıcılar: [Brave Browser] | [Firefox] * [bazı tweaks](https://restoreprivacy.com/firefox-privacy/)* ile | [Tor]
- İzleme Yapmayan Arama Motorları: [DuckDuckGo] | [StartPage] | [SearX] *(self-hosted)* | [Qwant]
- VPN: [Mullvad] | [ProtonVPN] | [Windscribe] | [IVPN] *(daha iyisi, anonimlik için [Tor] kullanın)*. Ayrıca bakınız [VPN Uyarı Notu]
- Uygulama Güvenlik Duvarı: [NetGuard] (Android) | [Lockdown] (iOS) | [OpenSnitch] (Linux) | [LuLu] (MacOS)

#### Tarayıcı Uzantıları
- [Privacy Badger] - İzleyicileri engeller.
- [HTTPS Everywhere] - İstekleri HTTPS'ye yükseltir.
- [uBlock Origin] - Reklamları, izleyicileri ve kötü amaçlı yazılımları engeller.
- [ScriptSafe] - Belirli komut dosyalarının yürütülmesini engeller.
- [WebRTC Leak Prevent] - IP sızıntılarını önler.
- Vanilla Cookie Manager] - İstenmeyen çerezleri otomatik olarak kaldırır.
- [Privacy Essentials] - Hangi sitelerin güvensiz olduğunu gösterir

#### Mobil Uygulamalar
- [Exodus] - Cihazınızda hangi izleyicilerin olduğunu gösterir.
- [Orbot]- Sistem genelinde Tor Proxy.
- [Island] - Uygulamalar için kum kutusu ortamı.
- [NetGuard] - Hangi uygulamaların ağ erişimine sahip olduğunu kontrol eder.
- [Bouncer] - Geçici izinler verin.
- [Greenify] - Hangi uygulamaların arka planda çalışabileceğini kontrol edin.
- [1.1.1.1] - CloudFlare'in HTTPS üzerinden DNS'sini kullanın.
- [Fing App] - Ev WiFi ağınızı davetsiz misafirlere karşı izleyin

#### Çevrimiçi Araçlar
- [εxodus] - Bir uygulamanın hangi izleyicilere sahip olduğunu gösterir.
- [';--have i been pwned?] - Bilgilerinizin bir ihlalde açığa çıkıp çıkmadığını kontrol edin.
- [EXIF Remover] - Görüntü veya dosyadan meta verileri kaldırır.
- [Yönlendirme Dedektifi] - Bağlantının nereye yönlendirildiğini gösterir.
- [Virus Total] - Dosya veya URL'yi kötü amaçlı yazılımlara karşı tarar.
- [Panopticlick], [Tarayıcı Sızıntı Testi] ve [IP Sızıntı Testi] - Sistem ve tarayıcı sızıntılarını kontrol edin

#### Üretkenlik Araçları
- Dosya Depolama: [NextCloud].
- Dosya Senkronizasyonu: [Syncthing].
- Dosya Bırakma: [FilePizza].
- Notlar: [Standart Notlar], [Cryptee], [Joplin].
- Bloglama: [Özgürce Yaz].
- Takvim / Kişiler Senkronizasyonu: [ETE Sync]

📜 **Daha Fazlasına Bakın**: [Gizliliğe Saygı Duyan Yazılımların Tam Listesi](https://github.com/Lissy93/awesome-privacy)

----

## DONANIM GÜVENLİĞİ

Fiziksel ve dijital güvenliğinizi artırmanıza yardımcı olabilecek bazı araçlar da vardır.

- **Engelleyiciler ve Kalkanlar**: [PortaPow] - USB Veri Engelleyici | [Mic-Block] - Mikrofonu fiziksel olarak devre dışı bırakır | [Silent-Pocket] - Sinyal engelleyici faraday poşetleri | [Lindy] - Fiziksel port engelleyiciler | [RFID Kalkanları] | [Webcam Kapakları] | [Gizlilik Ekranı]
- **Kripto Cüzdanlar**: [Trezor] - Donanım cüzdanı | [CryptoSteel] - Yok edilemez çelik kripto cüzdanı
- **FIDO U2F Anahtarları**: [Solo Anahtar] | [Nitro Anahtar] | [Librem Anahtar]
- Veri Engelleyiciler**: [PortaPow] - Kötü amaçlı yazılım yükleme saldırılarına karşı korumak için verileri engeller, FastCharge'ı etkinleştirir.
- **Donanım şifreli depolama**:  [iStorage]- PIN doğrulamalı 256 bit donanım şifreli depolama | [Şifreli Sürücü Muhafazası]
- **Ağ İletişimi**: [Anonabox] - Tak ve çalıştır Tor yönlendirici | [FingBox] - Kolay ev ağı otomatik güvenlik izleme
- **Paranoid Aletler** [Orwl]- Kendi kendini yok eden bilgisayar | [Hunter-Cat]- Kart-kaymağı dedektörü | [Adversarial Fashion]- Yüz tanıma önleyici giysi | [DSTIKE Deauth Detector] - Deauth saldırılarını tespit eder, Spacehuhn]'dan | [Reflectacles]- Gözetleme önleyici gözlük | [Armourcard]- Aktif RFID karıştırma | [Bug-Detector]- RF özellikli gizli dinleme ekipmanı olup olmadığını kontrol edin | [Ultrasonic Microphone Jammer] - İnsanlar için sessiz olan ancak kayıt ekipmanına müdahale eden sinyaller yayar.


Para harcamanıza gerek yok - Bu ürünlerin çoğu açık kaynak kodlu yazılımlarla evde yapılabilir. İşte [DIY Security Gadgets](/6_Privacy_and-Security_Gadgets.md#diy-security-products) listesi.

📜 **Daha Fazlasına Bakın**: [Gizlilik ve Güvenlik Araçları](/6_Privacy_and-Security_Gadgets.md)

----

*Ziyaretiniz için teşekkürler, umarım burada faydalı bir şeyler bulmuşsunuzdur :) Katkılar memnuniyetle karşılanır ve çok takdir edilir - bir düzenleme önermek için [raise an issue](https://github.com/Lissy93/personal-security-checklist/issues/new/choose) veya [open a PR](https://github.com/Lissy93/personal-security-checklist/pull/new/master). Bakınız: [`CONTRIBUTING.md`](/.github/CONTRIBUTING.md).*

----

Found this helpful? Consider sharing, to help others improve their digital security 😇

[![Twitter'da paylaşın](https://img.shields.io/badge/Share-Twitter-17a2f3?style=for-the-badge&logo=Twitter)](http://twitter.com/share?text=Check%20out%20the%20Personal%20Cyber%20Security%20Checklist-%20an%20ultimate%20list%20of%20tips%20for%20protecting%20your%20digital%20security%20and%20privacy%20in%202020%2C%20with%20%40Lissy_Sykes%20%F0%9F%94%90%20%20%F0%9F%9A%80&url=https://github.com/ClimpyX/siber-guvenlik-checklist)
[![LinkedIn'de paylaşın](https://img.shields.io/badge/Share-LinkedIn-0077b5?style=for-the-badge&logo=LinkedIn)](
http://www.linkedin.com/shareArticle?mini=true&url=hhttps://github.com/ClimpyX/siber-guvenlik-checklist&title=The%20Ultimate%20Personal%20Cyber%20Security%20Checklist&summary=%F0%9F%94%92%20A%20curated%20list%20of%20100%2B%20tips%20for%20protecting%20digital%20security%20and%20privacy%20in%202020&source=https://github.com/ClimpyX/siber-guvenlik-checklist)
[![Facebook'da paylaşın](https://img.shields.io/badge/Share-Facebook-4267b2?style=for-the-badge&logo=Facebook)](https://www.linkedin.com/shareArticle?mini=true&url=https://github.com/ClimpyX/siber-guvenlik-checklist&title=The%20Ultimate%20Personal%20Cyber%20Security%20Checklist&summary=%F0%9F%94%92%20A%20curated%20list%20of%20100%2B%20tips%20for%20protecting%20digital%20security%20and%20privacy%20in%202020&source=)
[![Mastodon'da paylaşın](https://img.shields.io/badge/Share-Mastodon-56a7e1?style=for-the-badge&logo=Mastodon)](https://mastodon.social/web/statuses/new?text=Check%20out%20the%20Ultimate%20Personal%20Cyber%20Security%20Checklist%20by%20%40Lissy93%20on%20%23GitHub%20%20%F0%9F%94%90%20%E2%9C%A8)




*Licensed under [Creative Commons, CC BY 4.0](https://creativecommons.org/licenses/by/4.0/), © [Alicia Sykes](https://aliciasykes.com) 2020*

<a href="https://twitter.com/intent/follow?screen_name=Lissy_Sykes">
  <img src="https://img.shields.io/twitter/follow/Lissy_Sykes?style=social&logo=twitter" alt="Follow Alicia Sykes on Twitter">
</a>


[//]: # (GUVENLIK YAZILIMLARINA AIT LINKLER)
[BitWarden]: https://bitwarden.com
[1Password]: https://1password.com
[KeePassXC]: https://keepassxc.org
[LessPass]: https://lesspass.com
[Aegis]: https://getaegis.app
[AndOTP]: https://github.com/andOTP/andOTP
[Authenticator]: https://mattrubin.me/authenticator
[VeraCrypt]: https://www.veracrypt.fr
[Cryptomator]: https://cryptomator.org
[Tor]: https://www.torproject.org
[Pi-Hole]: https://pi-hole.net
[Mullvad]: https://mullvad.net
[ProtonVPN]: https://protonvpn.com
[Windscribe]: https://windscribe.com/?affid=6nh59z1r
[IVPN]: https://www.ivpn.net
[NetGuard]: https://www.netguard.me
[Lockdown]: https://lockdownhq.com
[OpenSnitch]: https://github.com/evilsocket/opensnitch
[LuLu]: https://objective-see.com/products/lulu.html
[SimpleWall]: https://github.com/henrypp/simplewall
[33Mail]: http://33mail.com/Dg0gkEA
[anonaddy]: https://anonaddy.com
[Signal]: https://signal.org
[KeyBase]: https://keybase.io
[ProtonMail]: https://protonmail.com
[MailFence]: https://mailfence.com
[Tutanota]: https://tutanota.com
[Brave Browser]: https://brave.com/?ref=ali721
[Firefox]: https://www.mozilla.org/
[DuckDuckGo]: https://duckduckgo.com
[StartPage]: https://www.startpage.com
[Qwant]: https://www.qwant.com
[SearX]: https://asciimoo.github.io/searx

[VPN Warning Note]: https://github.com/Lissy93/personal-security-checklist/blob/master/5_Privacy_Respecting_Software.md#word-of-warning-8

[//]: # (ÜRETKENLIK YAZILIMI BAĞLANTILARI)
[NextCloud]: https://nextcloud.com
[Standard Notes]: https://standardnotes.org/?s=chelvq36
[Cryptee]: https://crypt.ee
[Joplin]: https://joplinapp.org
[ETE Sync]: https://www.etesync.com/accounts/signup/?referrer=QK6g
[FilePizza]: https://file.pizza/
[Syncthing]: https://syncthing.net
[Write Freely]: https://writefreely.org

[//]: # (TARAYICI UZANTISI BAĞLANTILARI)
[Privacy Badger]: https://www.eff.org/privacybadger
[HTTPS Everywhere]: https://eff.org/https-everywhere
[uBlock Origin]: https://github.com/gorhill/uBlock
[ScriptSafe]: https://github.com/andryou/scriptsafe
[WebRTC Leak Prevent]: https://github.com/aghorler/WebRTC-Leak-Prevent
[Vanilla Cookie Manager]: https://github.com/laktak/vanilla-chrome
[Privacy Essentials]: https://duckduckgo.com/app

[//]: # (ÇEVRIMIÇI GÜVENLIK ARAÇLARI)
[';--have i been pwned?]: https://haveibeenpwned.com
[εxodus]: https://reports.exodus-privacy.eu.org
[Panopticlick]: https://panopticlick.eff.org
[Browser Leak Test]: https://browserleaks.com
[IP Leak Test]: https://ipleak.net
[EXIF Remover]: https://www.exifremove.com
[Redirect Detective]: https://redirectdetective.com
[Virus Total]: https://www.virustotal.com

[//]: # (ANDROID UYGULAMA BAĞLANTILARI)
[Island]: https://play.google.com/store/apps/details?id=com.oasisfeng.island
[Orbot]: https://play.google.com/store/apps/details?id=org.torproject.android
[Orbot]: https://play.google.com/store/apps/details?id=org.torproject.android
[Bouncer]: https://play.google.com/store/apps/details?id=com.samruston.permission
[Crypto]: https://play.google.com/store/apps/details?id=com.kokoschka.michael.crypto
[Cryptomator]: https://play.google.com/store/apps/details?id=org.cryptomator
[Daedalus]: https://play.google.com/store/apps/details?id=org.itxtech.daedalus
[Brevent]: https://play.google.com/store/apps/details?id=me.piebridge.brevent
[Greenify]: https://play.google.com/store/apps/details?id=com.oasisfeng.greenify
[Secure Task]: https://play.google.com/store/apps/details?id=com.balda.securetask
[Tor Browser]: https://play.google.com/store/apps/details?id=org.torproject.torbrowser 
[PortDroid]: https://play.google.com/store/apps/details?id=com.stealthcopter.portdroid
[Packet Capture]: https://play.google.com/store/apps/details?id=app.greyshirts.sslcapture
[SysLog]: https://play.google.com/store/apps/details?id=com.tortel.syslog
[Dexplorer]: https://play.google.com/store/apps/details?id=com.dexplorer
[Check and Test]: https://play.google.com/store/apps/details?id=com.inpocketsoftware.andTest
[Tasker]: https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm
[Haven]: https://play.google.com/store/apps/details?id=org.havenapp.main
[NetGaurd]: https://www.netguard.me/
[Exodus]: https://exodus-privacy.eu.org/en/page/what/#android-app
[XUMI Security]: https://xumi.ca/xumi-security/
[Fing App]: https://www.fing.com/products/fing-app
[FlutterHole]: https://github.com/sterrenburg/flutterhole
[1.1.1.1]: https://1.1.1.1/
[The Guardian Project]: https://play.google.com/store/apps/dev?id=6502754515281796553
[The Tor Project]: https://play.google.com/store/apps/developer?id=The+Tor+Project
[Oasis Feng]: https://play.google.com/store/apps/dev?id=7664242523989527886
[Marcel Bokhorst]: https://play.google.com/store/apps/dev?id=8420080860664580239

[//]: # (GÜVENLIK DONANIM BAĞLANTILARI)
[Encrypted Drive Enclosure]: https://www.startech.com/HDD/Enclosures/encrypted-sata-enclosure-2-5in-hdd-ssd-usb-3~S2510BU33PW
[iStorage]: https://istorage-uk.com
[PortaPow]: https://portablepowersupplies.co.uk/product/usb-data-blocker
[Lindy]: https://lindy.com/en/technology/port-blockers
[Mic Block]: https://www.aliexpress.com/item/4000542324471.html
[RFID Shields]: https://www.aliexpress.com/item/32976382478.html
[Webcam Covers]: https://www.aliexpress.com/item/4000393683866.html
[Privacy Screen]: https://www.aliexpress.com/item/32906889317.html
[Trezor]: https://trezor.io
[CryptoSteel]: https://cryptosteel.com/product/cryptosteel/?v=79cba1185463
[Solo Key]: https://solokeys.com
[Nitro Key]: https://www.nitrokey.com
[Librem Key]: https://puri.sm/products/librem-key
[Anonabox]: https://www.anonabox.com
[FingBox]: https://www.fing.com/products/fingbox
[Orwl]: https://orwl.org
[Hunter-Cat]: https://lab401.com/products/hunter-cat-card-skimmer-detector
[DSTIKE Deauth Detector]: https://www.tindie.com/products/lspoplove/dstike-deauth-detector-pre-flashed-with-detector
[Bug-Detector]: https://www.brickhousesecurity.com/counter-surveillance/multi-bug
[Ultrasonic Microphone Jammer]: https://uspystore.com/silent-ultrasonic-microphone-defeater
[Silent-Pocket]: https://silent-pocket.com
[Armourcard]: https://armourcard.com
[Adversarial Fashion]: https://adversarialfashion.com
[Reflectacles]: https://www.reflectacles.com
[Spacehuhn]: https://github.com/spacehuhn/DeauthDetector

