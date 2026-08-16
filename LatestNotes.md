# LatestNotes — ISTQB Foundation Level (v4.0) Hata Analizi ve Çalışma Notları

Bu doküman, A/B/C/D örnek sınavlarında yanlış yapılan **68 sorunun** her biri için;
doğru şıkkın neden doğru, işaretlenen şıkkın neden yanlış olduğunu ve ikisi arasındaki
ayırt edici farkı ISTQB FL v4.0 syllabus'una dayanarak açıklar.

> **Kaynak güvencesi:** Bu dokümandaki `> ALINTI:` satırlarının tamamı `FoundationNotes.pdf`
> metninde **birebir** bulunduğu programatik olarak doğrulanmıştır. Syllabus'ta doğrudan
> karşılığı olmayan noktalar `KAYNAK YOK` olarak açıkça işaretlenmiştir — hiçbir dayanak
> uydurulmamıştır.

## Skor Tablosu

| Sınav | Doğru | Yanlış | Başarı | Eşik (%65) |
|:---|---:|---:|---:|:---|
| A | 24/40 | 16 | %60.0 | ❌ 2 soru eksik |
| B | 27/40 | 13 | %67.5 | ✅ geçer |
| C | 16/40 | 24 | %40.0 | ❌ 10 soru eksik |
| D | 25/40 | 15 | %62.5 | ❌ 1 soru eksik |
| **Toplam** | **92/160** | **68** | **%57.5** | — |

## Öncelikli Çalışma Sırası

Yanlış yoğunluğuna göre sıralanmıştır — en üstteki konu en çok puan kaybettiren konudur.

| Sıra | Syllabus bölümü | Yanlış | Toplam içindeki payı |
|---:|:---|---:|---:|
| 1 | 5 Test Faaliyetlerinin Yönetimi | 19 | %28 |
| 2 | 4 Test Analizi ve Tasarımı | 18 | %26 |
| 3 | 1 Testin Temelleri | 13 | %19 |
| 4 | 2 Yaşam Döngüsü Boyunca Test | 7 | %10 |
| 5 | 3 Statik Test | 7 | %10 |
| 6 | 6 Test Araçları | 4 | %6 |

### Aynı öğrenme hedefinde tekrarlanan hatalar

Bu hedefler birden fazla sınavda yanlış yapıldı — kavram gerçekten oturmamış demektir.

| Öğrenme hedefi | Kez | Sorular |
|:---|---:|:---|
| `FL-5.1.5` | 4 | A-33, B-32, C-32, D-32 |
| `FL-6.1.1` | 4 | A-39, B-39, C-39, D-39 |
| `FL-1.4.1` | 3 | A-4, C-4, D-4 |
| `FL-1.4.5` | 3 | A-6, C-6, D-6 |
| `FL-1.5.2` | 3 | A-8, C-7, D-7 |
| `FL-4.2.1` | 3 | A-20, B-20, C-20 |
| `FL-4.2.2` | 3 | A-21, B-21, C-21 |
| `FL-3.1.2` | 2 | A-15, D-16 |
| `FL-3.2.4` | 2 | A-17, C-17 |
| `FL-5.1.3` | 2 | A-31, B-30 |
| `FL-5.4.1` | 2 | A-37, C-37 |
| `FL-2.1.2` | 2 | B-10, D-9 |
| `FL-4.1.1` | 2 | B-19, D-19 |
| `FL-4.4.3` | 2 | B-27, C-27 |
| `FL-5.1.7` | 2 | C-34, D-33 |
| `FL-5.3.2` | 2 | C-36, D-36 |
| `FL-5.5.1` | 2 | C-38, D-38 |

### Tekrar eden kavram yanılgıları

Farklı sorularda aynı düşünce hatasının tekrarı. Bunları düzeltmek en yüksek getiriyi sağlar.

| Yanılgı | Görüldüğü sorular |
|:---|:---|
| `test-aktivite-siniri-karisikligi` | A-4, C-4, C-5, D-4 |
| `test-yonetimi-vs-test-etme-rolu` | A-6, C-6, D-6 |
| `tum-ekip-yaklasimi-yanlis-anlasilmasi` | A-8, C-7, D-7 |
| `degildir-sorusunda-dogru-ifadeyi-isaretleme` | A-15, A-18 |
| `gozden-gecirme-turleri-karisikligi` | A-17, C-17 |
| `hata-tahmini-kesif-testi-karisikligi` | A-27, C-26 |
| `siralama-sorusunda-ordinal-atlama` | A-33, C-32 |
| `test-ceyrekleri-test-seviyesi-karisikligi` | C-34, D-33 |
| `hata-raporu-vs-diger-surec-ciktisi-karisikligi` | C-37, D-36 |
| `hata-raporu-kritik-alan-onceliklendirme` | C-38, D-38 |

### Çok cevaplı sorularda özel durumlar

| Soru | İşaretlenen | Doğru | Durum |
|:---|:---|:---|:---|
| A-6 | `a,d` | `a,e` | Doğru şıklardan biri yakalanmış, diğeri kaçırılmış. |
| A-31 | `c` | `c,e` | Doğru şıklardan biri yakalanmış, diğeri kaçırılmış. |
| C-4 | `a` | `b,e` | İki şık gerekirken tek şık işaretlenmiş. |

---

# Soru Bazında Ayrıntılı Analiz


## Bölüm 1 — Testin Temelleri  (13 soru)

### A-4 · FL-1.4.1 · K2
**Senin cevabın:** a · **Doğru cevap:** b

**Neyi soruyor:** Verilen dört somut faaliyetten hangisinin **test analizi** aktivitesine ait olduğunu soruyor. Yani "test koşullarını belirleme/önceliklendirme" işini diğer aktivitelerden ayırt edebiliyor musun?

**Doğru şık neden doğru:** "Ödemenin birden fazla kullanıcı arasında düzgün paylaştırılıp paylaştırılmadığını **test etmeye karar vermek**" tam olarak bir *test koşulu* tanımlamaktır — yani "ne test edilecek?" sorusunun cevabıdır. Bu, test analizinin çekirdek görevidir.

> ALINTI: "Test analizi test edilebilir özellikleri belirlemek ve ilgili riskler ve risk seviyeleri ile birlikte ilişkili test"

> ALINTI: "koşullarını tanımlamak ve önceliklendirmek üzere test esasının analiz edilmesini içerir (bkz. bölüm 5.2)."

**Senin şıkkın neden yanlış:** (a) "8 adam/gün süreceğini tahmin etmek" bir **efor tahminlemesi**dir; tahminleme, yaklaşım ve kaynak belirleme **test planlama** aktivitesine aittir (detayı 5.1'dedir), test analizine değil.

> ALINTI: "Test planlama test hedefini belirleyip ardından genel bağlam dahilinde gerekli olan kısıtlar kapsamında"

Ayrıca diğer çeldiriciler de farklı aktiviteleri tarif ediyor: (c) BVA ile test verisi oluşturmak → test tasarımı/test uyarlama; (d) gerçekleşen ile beklenen sonucu karşılaştırıp hata raporu yazmak → test koşumu.

> ALINTI: "sonuçları beklenen sonuçlarla karşılaştırılır. Test sonuçları kaydedilir. Olası nedenlerin belirlenmesi için"

**Ayırt edici fark:** Test analizi **"ne test edilecek"** sorusunu cevaplar (test koşulu belirleme); efor/süre tahmini ise **test planlamanın** işidir.

**Yanılgı etiketi:** `test-aktivite-siniri-karisikligi`

---
### A-6 · FL-1.4.5 · K2
**Senin cevabın:** a,d · **Doğru cevap:** a,e

**Durum: KISMİ DOĞRU.** (a) Test ortamlarını yapılandırmak şıkkını **doğru** yakalamışsın — bu gerçekten test etme rolüne ait. Kaybettiğin yer ikinci şık.

**Neyi soruyor:** Beş görevden hangi ikisinin **ESAS OLARAK test etme rolüne** (tester) ait olduğunu soruyor. Ayrım noktası: test etme rolü = testin mühendislik/teknik tarafı.

**Doğru şık neden doğru:** Test etme rolü test analizi, test tasarımı, test uyarlama ve test koşumuna odaklanır. (e) "Test esasını analiz etmek" doğrudan **test analizi**dir, (a) "test ortamlarını yapılandırmak" ise **test uyarlama** aktivitesinin bir görevidir — ikisi de bu dört aktivitenin içindedir.

> ALINTI: "Test etme rolü testin mühendislik (teknik) yönünün tüm sorumluluğuna sahiptir. Test etme rolü temelde"

> ALINTI: "test analizi, test tasarımı, test uyarlama ve test koşumu aktivitelerine odaklanır."

> ALINTI: "Test ortamı oluşturulur ve kurulumunun uygun"

**Senin şıkkın neden yanlış:** (d) "Test planını oluşturmak" **test planlama** aktivitesidir ve syllabus bunu açıkça **test yönetimi rolüne** verir; test etme rolüne değil.

> ALINTI: "sorumludur. Test yönetimi rolü temelde test planlama, test gözetimi ve kontrolü ve test tamamlama"

(b) ürün backlog'u yönetmek ve (c) yeni gereksinimlere çözüm tasarlamak zaten test rolleri değildir (ürün sahibi / yazılımcı işi).

**Ayırt edici fark:** Test **esasını analiz etmek** teknik/mühendislik işidir → test etme rolü; test **planını oluşturmak** yönetsel iştir → test yönetimi rolü.

**Yanılgı etiketi:** `test-yonetimi-vs-test-etme-rolu` `cok-cevapli-soruda-eksik-secim`

---
### A-8 · FL-1.5.2 · K1
**Senin cevabın:** b · **Doğru cevap:** d

**Neyi soruyor:** Tüm ekip yaklaşımında **test uzmanları ile iş birimleri (business)** arasındaki iş birliğinin syllabus'taki tipik örneğinin ne olduğunu soruyor.

**Doğru şık neden doğru:** Syllabus bu iş birliğini iki ayrı muhataba böler ve **iş birimleriyle olan iş birliğinin örneğini "uygun kabul testleri oluşturmak"** olarak verir. Şık (d) bu cümlenin birebir karşılığıdır.

> ALINTI: "Bu, uygun kabul testleri oluşturmalarına yardımcı olmak için iş birimleriyle iş birliği yapmanın"

**Senin şıkkın neden yanlış:** (b) "Test uzmanları, iş birimlerinin **test stratejisini** tanımlamasına yardımcı olur" — syllabus'ta test stratejisi ve test otomasyonu metodolojisi kararı iş birimleriyle değil, **yazılımcılarla** birlikte alınır. Doğru kavramı seçmişsin ama **yanlış muhataba** bağlamışsın.

> ALINTI: "yanı sıra test stratejisi ve test otomasyonu metodolojilerine karar vermek için yazılımcılarla birlikte"

**Ayırt edici fark:** İş birimleriyle → **kabul testleri**; yazılımcılarla → **test stratejisi ve test otomasyonu**.

**Yanılgı etiketi:** `tum-ekip-yaklasimi-yanlis-anlasilmasi`

---
### C-1 · FL-1.1.1 · K1
**Senin cevabın:** a · **Doğru cevap:** b

**Neyi soruyor:** Syllabus'un 1.1.1'de madde madde saydığı **genel test hedefleri** listesinden hangisinin şıklarda geçtiğini soruyor.

**Doğru şık neden doğru:** (b) "Arızalara neden olmak ve hataları bulmak", listedeki maddenin neredeyse kelimesi kelimesine karşılığıdır.

> ALINTI: "Arızaları tetiklemek ve hataları bulmak"

**Senin şıkkın neden yanlış:** (a) "Dokümante edilmiş gereksinimlerin **karşılandığını** doğrulamak" — syllabus'taki hedef "gereksinimlerin karşılandığını kanıtlamak" değil, "**yerine getirilip getirilmediğini**" kontrol etmektir. Test, gereksinimlerin sağlandığını *ispatlamak* için değil, sağlanıp sağlanmadığını *sınamak* için yapılır; hata olmadığını ispatlamak zaten Prensip 1'e aykırıdır.

> ALINTI: "Belirtilen gereksinimlerin yerine getirilip getirilmediğini doğrulamak"

> ALINTI: "Testler, test nesnesinde hataların mevcut olduğunu gösterebilir ancak hiç hata kalmadığını"

Aynı kusur (d) şıkkında da var; (c) ise "hataları başlatmak ve kök nedenleri belirlemek" diyerek **hata ayıklama** (debugging) faaliyetini tarif eder — bu bir test hedefi değildir.

> ALINTI: "Dinamik test (bkz. konu 4) bir arızayı tetiklediğinde hata ayıklama işlemi bu arızanın (hataların)"

**Ayırt edici fark:** Doğru şık testin **hata bulma** hedefini ifade eder; senin şıkkın testi "gereksinimlerin sağlandığını kanıtlama" işi gibi göstererek testin ispat gücünü olduğundan fazla varsayar.

**Yanılgı etiketi:** `test-hedefleri-ile-dogrulama-karisikligi`

---
### C-3 · FL-1.3.1 · K2
**Senin cevabın:** a · **Doğru cevap:** b

**Neyi soruyor:** **Prensip 7 — "Yeni hata bulamıyoruz, başarılı yazılım elde ettik" yanılgısı** prensibinin *pratikteki* uygulaması hangisidir?

**Doğru şık neden doğru:** Prensip 7'nin özü şudur: tüm gereksinimleri test edip tüm hataları düzeltmek bile kullanıcının gerçek ihtiyaçlarını karşılamayan bir yazılımı engellemez; bu yüzden doğrulamanın (verification) yanında **sağlama (validation)** da yapılmalıdır. (b) "Son kullanıcıları kabul testlerini gerçekleştirmeleri için desteklemek", sağlamayı pratiğe geçiren tam da bu davranıştır.

> ALINTI: "Yeni hata bulamıyoruz başarılı bir yazılım elde ettik yanılgısı."

> ALINTI: "kullanıcıların ihtiyaçlarını ve beklentilerini karşılamayan,"

> ALINTI: "Test sırasında doğrulamanın yanında sağlama da"

**Senin şıkkın neden yanlış:** (a) "Testlerin, hata olmadığını gösteremeyeceğini açıklamak" doğru bir ifadedir ama **Prensip 1**'i (testin amacı hataların varlığını göstermektir) anlatır, Prensip 7'yi değil. Soru senden belirli bir prensibin uygulamasını istiyordu.

> ALINTI: "Testler, test nesnesinde hataların mevcut olduğunu gösterebilir ancak hiç hata kalmadığını"

(c) "hiçbir hatanın kalmadığından emin olmak" zaten imkânsızdır; (d) arızaya yol açmayan testleri "daha az hata var" varsayımıyla değiştirmek prensibin çarpıtılmış hâlidir.

**Ayırt edici fark:** Prensip 1 = testin **ispat gücünün sınırı**; Prensip 7 = hatasız olmanın **kullanıcı ihtiyacını karşılamaya yetmemesi**, yani sağlama ihtiyacı.

**Yanılgı etiketi:** `test-prensipleri-arasi-karisiklik`

---
### C-4 · FL-1.4.1 · K2
**Senin cevabın:** a · **Doğru cevap:** b,e

**Durum: EKSİK SEÇİM.** İki şık istenirken bir şık işaretlemişsin; ayrıca işaretlediğin şık da doğru kümenin dışında kaldığı için bu sorudan puan çıkmıyor.

**Neyi soruyor:** Sınır değer analizi (BVA) ve denklik paylarına ayırma gibi **test tekniklerinin** en çok hangi iki test aktivitesinde kullanıldığını soruyor.

**Doğru şık neden doğru:** Syllabus test tekniklerini iki aktivitede açıkça anar: **test analizi** (test koşullarını belirlerken tekniklerle desteklenir) ve **test tasarımı** (test koşullarını test senaryolarına dönüştürürken teknikler kullanılır).

> ALINTI: "Test analizi genellikle test tekniklerinin kullanımıyla desteklenir (bkz. konu 4)."

> ALINTI: "Test tasarımı test koşullarının test senaryoları ve diğer test çalışma ürünleri olarak detaylandırılmasını"

> ALINTI: "kapsam öğelerinin belirlenmesini içerir. Test teknikleri (bkz. konu 4) bu aktiviteyi"

**Senin şıkkın neden yanlış:** (a) "Test uygulaması" = syllabus'taki **test uyarlama**dır; bu aktivite tekniklerle senaryo *türetmez*, tasarımı bitmiş testleri koşuma **hazırlar** (test verisini edinme, prosedürleri düzenleme, ortamı kurma). Teknik uygulanması değil, hazırlık işidir.

> ALINTI: "Test uyarlama test koşumu için gerekli test çalışma ürünlerini oluşturmayı veya edinmeyi içerir"

Diğerleri de dışarıdadır: (c) test koşumu testleri çalıştırır, (d) test gözetimi ilerlemeyi izler.

> ALINTI: "Test gözetimi tüm test aktivitelerinin devamlı izlenmesini ve planlanan"

**Ayırt edici fark:** Teknikler **ne test edileceğini belirlerken (analiz)** ve **testi kurgularken (tasarım)** uygulanır; test uyarlama yalnızca kurgulanmış testi koşuma hazır hâle getirir.

**Yanılgı etiketi:** `test-aktivite-siniri-karisikligi` `cok-cevapli-soruda-eksik-secim`

---
### C-5 · FL-1.4.3 · K2
**Senin cevabın:** b · **Doğru cevap:** a

**Neyi soruyor:** Dört **test çalışma ürününü** üretildikleri test aktiviteleriyle eşleştirmeyi istiyor. Doğru eşleşme: 1B, 2D, 3C, 4A.

**Doğru şık neden doğru:** Syllabus 1.4.3'te çalışma ürünlerini aktivite aktivite listeler:

- **1. Kapsam öğeleri → B (Test tasarımı)**
> ALINTI: "belgeleri, kapsam öğeleri, test verisi gereksinimleri ve test ortamı gereksinimleri."

- **2. Değişiklik istekleri → D (Test tamamlama)**
> ALINTI: "proje veya döngülerin iyileştirilmesine yönelik aksiyon öğeleri, tecrübeler ve değişiklik talepleri"

- **3. Test yürütme (koşum) çizelgesi → C (Test uygulaması / test uyarlama)**
> ALINTI: "test grupları, test verisi, test koşumu çizelgesi ve test ortamı öğeleri."

- **4. Önceliklendirilmiş test koşulları → A (Test analizi)**
> ALINTI: "•  Test analizi iş ürünleri şunları içerir: (önceliklendirilmiş) test koşulları"

**Senin şıkkın neden yanlış:** (b) 1B ve 2D'yi doğru kurmuşsun; hatan **3 ve 4'ü ters çevirmen**: test koşum çizelgesini test *analizine*, önceliklendirilmiş test koşullarını ise test *uygulamasına* bağlamışsın. Oysa çizelge koşuma hazırlık ürünüdür (uyarlama), test koşulları ise analizin çıktısıdır.

> ALINTI: "Test prosedürleri, etkin test koşumu için test koşum çizelgesi"

**Ayırt edici fark:** **Test koşulu** = analizin çıktısı ("ne test edilecek"); **test koşum çizelgesi** = uyarlamanın çıktısı ("hangi test ne zaman koşulacak").

**Yanılgı etiketi:** `test-aktivite-siniri-karisikligi`

---
### C-6 · FL-1.4.5 · K2
**Senin cevabın:** b · **Doğru cevap:** c

**Neyi soruyor:** Test rolleri hakkındaki dört ifadeden EN DOĞRU olanı; özellikle Çevik ortamda test yönetiminin nasıl dağıldığını soruyor.

**Doğru şık neden doğru:** Syllabus, Çevik'te bazı test yönetimi görevlerinin ekibin kendisi tarafından, **birden fazla ekibi/organizasyonu ilgilendiren** görevlerin ise ekip dışındaki test yöneticileri tarafından yürütülebileceğini söyler. (c) bunun aynısıdır.

> ALINTI: "Yazılım Geliştirmede bazı test yönetimi görevleri Çevik ekip tarafından gerçekleştirilirken, birden fazla ekibi"

> ALINTI: "veya tüm organizasyonu ilgilendiren görevler geliştirme ekipleri dışındaki test yöneticileri tarafından yerine"

**Senin şıkkın neden yanlış:** (b) iki rolün odaklarını **ters çevirmiş**: test etme rolünü "test izleme ve kontrol"e, test yönetimi rolünü "planlama ve tamamlama"ya bağlıyor. Planlama **ve** gözetim/kontrol **ve** tamamlama üçü birden test yönetimi rolüne aittir; test etme rolü ise analiz–tasarım–uyarlama–koşuma odaklıdır.

> ALINTI: "sorumludur. Test yönetimi rolü temelde test planlama, test gözetimi ve kontrolü ve test tamamlama"

> ALINTI: "test analizi, test tasarımı, test uyarlama ve test koşumu aktivitelerine odaklanır."

(d) da aynı şekilde analiz/tasarımı yanlışlıkla test yönetimine verir; (a) ise test etme rolünü "ekip dışından tek kişi" diye tarif ederek tüm ekip yaklaşımına aykırı düşer.

**Ayırt edici fark:** Test **gözetimi ve kontrolü** test etme rolünün değil, **test yönetimi rolünün** üç odak aktivitesinden biridir.

**Yanılgı etiketi:** `test-yonetimi-vs-test-etme-rolu`

---
### C-7 · FL-1.5.2 · K1
**Senin cevabın:** a · **Doğru cevap:** b

**Neyi soruyor:** Tüm ekip yaklaşımının syllabus'ta sayılan **faydalarından** hangisi şıklarda geçiyor?

**Doğru şık neden doğru:** Syllabus faydaları tek cümlede sayar: ekip ilişkilerini geliştirir, iletişim ve iş birliğini artırır, farklı beceri setlerinin kullanımıyla sinerji yaratır. (b) "Gelişmiş ekip dinamikleri" bunun doğrudan karşılığıdır.

> ALINTI: "Tüm ekip yaklaşımı ekip ilişkilerini geliştirir, ekip içinde"

> ALINTI: "iletişimi ve iş birliğini artırır ve ekibin farklı beceri setlerinin proje yararına kullanılmasına olanak"

**Senin şıkkın neden yanlış:** (a) "Test uzmanı bulunmayan ekipler" — tüm ekip yaklaşımı test uzmanını ekipten **çıkarmaz**; tam tersine test uzmanını ekibin içine alır ve kalite sorumluluğunu herkese yayar. "Kaliteden herkes sorumludur" ifadesi "test uzmanına gerek yok" demek değildir.

> ALINTI: "Tüm ekip yaklaşımında, gerekli bilgi ve beceriye sahip tüm ekip üyeleri her türlü görevi yapabilir ve"

> ALINTI: "kaliteden herkes sorumludur."

(c) uzmanlaşmış ekip üyeleri ve (d) daha büyük ekipler syllabus'ta fayda olarak geçmez.

**Ayırt edici fark:** Fayda, kalite sorumluluğunun paylaşılmasıyla oluşan **iyileşmiş ekip dinamiği**dir; test uzmanı rolünün **ortadan kalkması** değil.

**Yanılgı etiketi:** `tum-ekip-yaklasimi-yanlis-anlasilmasi`

---
### D-2 · FL-1.2.3 · K2
**Senin cevabın:** a · **Doğru cevap:** c

**Neyi soruyor:** Bir senaryodaki olayları **insan hatası (error) – hata/kusur (defect) – arıza (failure) – kök neden (root cause)** zincirine doğru yerleştirmeni istiyor.

**Doğru şık neden doğru:** Kök neden, problemin ortaya çıkmasının temel sebebidir. Senaryoda programcının **yoğun zaman baskısı altında çalışması**, exception yönetimini koda eklememesine (yani hataya) yol açan temel durumdur — bu tanım gereği bir kök nedendir. Syllabus zaman baskısını, insanların hata yapma sebepleri arasında açıkça sayar.

> ALINTI: "Kök neden, bir problemin ortaya çıkmasının temel sebebidir (ör. hataya yol açan bir durum)."

> ALINTI: "İnsanlar  hata  (yanlışlık)  yapar  ve  bu  da  yazılım  hatalarına  (arıza,  hata)  neden  olur"

**Senin şıkkın neden yanlış:** (a) "Bonusların yanlış hesaplanması ... bir hatadır (defect)" — yanlış hesaplama, sistem çalışırken **gözlemlenen dış davranıştır**, yani bir **arızadır (failure)**. Hata (defect) olan şey koddaki **eksik exception yönetimidir**. Ayrıca "bazen ortaya çıkması" da tipik bir arıza davranışıdır: kimi hata belirli koşullarda arızaya yol açar.

> ALINTI: "Koddaki bir hata çalıştırılırsa sistem yapması gerekeni yapmayabilir veya yapmaması"

> ALINTI: "arızaya neden olurken, bazıları belirli koşullar altında arızaya neden olur, bazıları ise hiçbir zaman"

Diğerleri: (b) düzenleyici kurumun kestiği **ceza** bir arıza değil, arızanın **sonucudur**; arıza, arayüzün engelli kullanıcılar için düzgün çalışmamasıdır. (d) tasarım dokümanı bir **hata (defect)** içerir; "error" ise tasarımcının yaptığı insan yanlışlığıdır, dokümanın içinde durmaz.

> ALINTI: "Hatalar, gereksinim veya test betiği gibi dokümantasyonda, kaynak kodda veya derleme dosyası gibi"

**Ayırt edici fark:** **Defect** = üründeki (kod/doküman) kusurun kendisi; **failure** = çalışırken görünen yanlış davranış; **root cause** = o kusuru doğuran temel koşul (burada zaman baskısı).

**Yanılgı etiketi:** `hata-ariza-kok-neden-karisikligi`

---
### D-4 · FL-1.4.1 · K2
**Senin cevabın:** d · **Doğru cevap:** b

**Neyi soruyor:** Dört **test görevini** ait oldukları test aktiviteleriyle eşleştirmeyi istiyor. Doğru eşleşme: 1B, 2D, 3C, 4A.

**Doğru şık neden doğru:**

- **1. Test koşullarından test senaryoları türetmek → B (Test tasarımı)**
> ALINTI: "Test tasarımı test koşullarının test senaryoları ve diğer test çalışma ürünleri olarak detaylandırılmasını"

- **2. Yeniden kullanılabilir test varlıklarını belirlemek → D (Test tamamlama)**
> ALINTI: "Gelecekte faydalı olabilecek test çalışma ürünleri belirlenir ve arşivlenir ya da uygun ekiplere"

- **3. Test senaryolarını test prosedürleri hâline organize etmek → C (Test uygulama / test uyarlama)**
> ALINTI: "Test senaryoları test prosedürleri şeklinde düzenlenebilir ve test grupları halinde birleştirilebilir."

- **4. Test temelini ve test edilen ürünü değerlendirmek → A (Test analizi)**
> ALINTI: "Test esası ve test hedefleri aynı zamanda içerebilecekleri hataları belirlemek ve test edilebilirliği analiz"

**Senin şıkkın neden yanlış:** (d) = 1C, 2D, 3A, 4B. İçinde **yalnızca 2D doğru**. Üç hatan var: test senaryosu *türetmeyi* uyarlamaya (1C), senaryoları prosedüre *organize etmeyi* analize (3A), test esasını *değerlendirmeyi* tasarıma (4B) bağlamışsın. Yani tasarım–uyarlama–analiz üçlüsünü birbirine kaydırmışsın.

**Ayırt edici fark:** **Tasarım** test koşulundan test senaryosunu *üretir*; **uyarlama** var olan senaryoları prosedür/çizelge hâline *düzenler*; **analiz** ise test esasını *değerlendirip* test koşullarını çıkarır.

**Yanılgı etiketi:** `test-aktivite-siniri-karisikligi`

---
### D-6 · FL-1.4.5 · K2
**Senin cevabın:** a · **Doğru cevap:** d

**Neyi soruyor:** Verilen dört görevden hangisinin **test yönetimi rolünün** görevi olduğunu soruyor.

**Doğru şık neden doğru:** Test yönetimi rolü test planlama, test gözetimi/kontrolü ve **test tamamlama** aktivitelerine odaklanır; test tamamlama raporunu oluşturup paydaşlara iletmek bu aktivitenin çıktısıdır.

> ALINTI: "sorumludur. Test yönetimi rolü temelde test planlama, test gözetimi ve kontrolü ve test tamamlama"

> ALINTI: "Test tamamlama raporu oluşturulur ve paydaşlara iletilir."

**Senin şıkkın neden yanlış:** (a) "Test esasını ve test nesnesini değerlendirmek" **test analizi** görevidir; test analizi ise test etme rolünün odak aktivitelerinden biridir, test yönetiminin değil.

> ALINTI: "Test esası ve test hedefleri aynı zamanda içerebilecekleri hataları belirlemek ve test edilebilirliği analiz"

> ALINTI: "test analizi, test tasarımı, test uyarlama ve test koşumu aktivitelerine odaklanır."

Aynı gerekçeyle (b) test ortamı gereksinimlerini tanımlamak → test tasarımı ve (c) test edilebilirliği değerlendirmek → test analizi de test etme rolüne düşer.

> ALINTI: "belgeleri, kapsam öğeleri, test verisi gereksinimleri ve test ortamı gereksinimleri."

**Ayırt edici fark:** Test yönetimi rolünün dört aktiviteli listesi **planlama / gözetim–kontrol / tamamlama** etrafındadır; analiz–tasarım–uyarlama–koşum ise her zaman **test etme rolü**ne aittir.

**Yanılgı etiketi:** `test-yonetimi-vs-test-etme-rolu`

---
### D-7 · FL-1.5.2 · K1
**Senin cevabın:** d · **Doğru cevap:** a

**Neyi soruyor:** C-7 ile aynı bilgiyi farklı şıklarla soruyor: tüm ekip yaklaşımının syllabus'ta yazılı faydası nedir?

**Doğru şık neden doğru:** Syllabus, ortak çalışma alanının iletişim ve etkileşimi kolaylaştırdığını, yaklaşımın ekip içi iletişimi ve iş birliğini artırdığını söyler. (a) "Ekip üyeleri arasında iletişimin iyileşmesi" bunun birebir karşılığıdır.

> ALINTI: "çalışma alanı iletişim ve etkileşimi kolaylaştırır."

> ALINTI: "iletişimi ve iş birliğini artırır ve ekibin farklı beceri setlerinin proje yararına kullanılmasına olanak"

**Senin şıkkın neden yanlış:** (d) "Harici iş kullanıcılarıyla iş birliğinin **azalması**" faydanın tam tersidir; syllabus test uzmanlarının iş birimleriyle kabul testleri için **iş birliği yaptığını** söyler. (b) "kalite için bireysel sorumluluğun azalması" da terstir — kaliteden herkes sorumlu hâle gelir. (c) daha hızlı teslimat ise bu bölümde fayda olarak sayılmaz.

> ALINTI: "Bu, uygun kabul testleri oluşturmalarına yardımcı olmak için iş birimleriyle iş birliği yapmanın"

> ALINTI: "kaliteden herkes sorumludur."

**Ayırt edici fark:** Tüm ekip yaklaşımı iş birliğini ve sorumluluk paylaşımını **artırır**; senin şıkkın azalttığını iddia ediyor.

**Yanılgı etiketi:** `tum-ekip-yaklasimi-yanlis-anlasilmasi`

---

## Tekrar Eden Yanılgı Etiketleri (Bölüm 1)

| Etiket | Soru sayısı | Sorular |
|---|---|---|
| `test-aktivite-siniri-karisikligi` | 4 | A-4, C-4, C-5, D-4 |
| `test-yonetimi-vs-test-etme-rolu` | 3 | A-6, C-6, D-6 |
| `tum-ekip-yaklasimi-yanlis-anlasilmasi` | 3 | A-8, C-7, D-7 |
| `hata-ariza-kok-neden-karisikligi` | 1 | D-2 |
| `test-prensipleri-arasi-karisiklik` | 1 | C-3 |
| `test-hedefleri-ile-dogrulama-karisikligi` | 1 | C-1 |
| `cok-cevapli-soruda-eksik-secim` | 2 | A-6, C-4 |

## Bölüm 2 — Yazılım Geliştirme Yaşam Döngüsü Boyunca Test  (7 soru)

### A-11 · FL-2.1.5 · K2
**Senin cevabın:** a · **Doğru cevap:** d

**Neyi soruyor:** Verilen dört uygulamadan hangisinin "shift-left" (testi yaşam döngüsünde erkene çekme) yaklaşımının bir örneği OLMADIĞINI soruyor. Yani üç şık syllabus'taki shift-left iyi uygulamalarına karşılık geliyor, biri gelmiyor.

**Doğru şık neden doğru:** Shift-left, test faaliyetlerinin *geliştirme faaliyetlerine göre* daha erken yapılmasıyla ilgilidir; ölçüt "kod yazılmadan/bileşenler entegre edilmeden önce test etmek"tir.
> ALINTI: "Shift-left genellikle testlerin daha erken yapılmasını önerir"

Syllabus'un shift-left iyi uygulamaları listesinde yapılandırma yönetimi ile ilgili hiçbir madde yoktur; listedeki maddeler şunlardır:
> ALINTI: "Testçilerin bakış açısıyla analizin gözden geçirilmesi."

> ALINTI: "Kod yazılmadan önce test senaryolarının yazılması"

(d) şıkkındaki "yapılandırma yönetim süreci kurulmadan önce test betiği yazmak" ifadesi, testin geliştirmeye göre erkene çekilmesini değil, bir *destek/yönetim sürecinin* sırasını anlatır. Yapılandırma yönetimi syllabus'ta Bölüm 5 (test yönetimi) altında bir destek faaliyetidir, bir geliştirme aşaması değildir. Dolayısıyla bu bir shift-left örneği değildir; aksine, yapılandırma yönetimi kurulmadan üretilen test varlıklarının izlenebilirliği ve sürüm kontrolü sağlanamayacağı için kötü bir uygulamadır.

**Senin şıkkın neden yanlış:** (a) "Kullanıcı gereksinimlerini paydaşların kabulünden önce gözden geçirmek" tam olarak syllabus'un ilk shift-left maddesidir — testçi bakış açısıyla analizin/gereksinimlerin erken gözden geçirilmesi. Bu, statik test yoluyla belirsizlik ve eksiklikleri kod yazılmadan önce yakalamayı sağlar; yani soruda aranan "DEĞİLDİR" değil, tipik bir shift-left örneğidir. (b) kod öncesi bileşen testi yazmak = TDD/önce-test-et; (c) bileşen testi seviyesinde performans testi koşmak da açıkça shift-left olarak etiketlenir:
> ALINTI: "Bu bir tür shift-left uygulamasıdır."

**Ayırt edici fark:** Shift-left ölçütü "test faaliyeti geliştirme faaliyetinden önce mi geliyor?" sorusudur; (a), (b), (c) bu ölçütü karşılar, (d) ise testi erkene çekmez, yalnızca bir yönetim sürecinin eksikliğini tarif eder.

**Yanılgı etiketi:** `shift-left-kapsam-yanlis-genisletme`

---
### B-9 · FL-2.1.1 · K2
**Senin cevabın:** c · **Doğru cevap:** b

**Neyi soruyor:** Farklı YGYD modellerinin (sıralı, döngüsel, artımlı, Çevik) test faaliyetleri üzerindeki etkisine dair dört ifadeden hangisinin doğru olduğunu soruyor.

**Doğru şık neden doğru:** Sıralı modellerde çalıştırılabilir kod ancak geç aşamalarda oluştuğu için dinamik test erken yapılamaz; erken aşamalar statik faaliyetlerle (gözden geçirme, test analizi, test tasarımı) doludur.
> ALINTI: "Sıralı yazılım geliştirme modellerinde, ilk aşamalarda test uzmanları genellikle gereksinim gözden"

> ALINTI: "bu nedenle tipik olarak dinamik testler YGYD'nin erken aşamalarında gerçekleştirilemez."

Bu, (b) şıkkındaki "dinamik testler genellikle yaşam döngüsünün ilerleyen aşamalarıyla sınırlandırılır" ifadesinin birebir karşılığıdır.

**Senin şıkkın neden yanlış:** (c) "Yinelemeli (döngüsel) modelde bileşen testleri genellikle geliştiriciler tarafından **manuel olarak** gerçekleştirilir." Cümlenin "geliştiriciler tarafından" kısmı doğrudur:
> ALINTI: "normalde geliştiriciler tarafından kendi geliştirme ortamlarında yapılır."

Ancak "manuel olarak" kısmı yanlıştır. Döngüsel/artımlı modellerde sık teslimat, kapsamlı ve otomatik regresyon testi gerektirir; bileşen testleri birim test çerçeveleriyle otomatikleştirilir.
> ALINTI: "Yazılım özelliklerinin sık hayata geçirilmesi hızlı"

> ALINTI: "projelerde iş ürünü belgelerinin hafifletilmesi ve regresyon testlerini kolaylaştırmak için kapsamlı test"

Ayrıca (a) yanlıştır çünkü otomasyon regresyon testi *ihtiyacını* ortadan kaldırmaz, yalnızca onu uygulama biçimidir; (d) yanlıştır çünkü artımlı modelde statik VE dinamik testler her artımda birlikte yapılabilir, "statik erken / dinamik sonra" ayrımı sıralı modelin özelliğidir.

**Ayırt edici fark:** (b) modelin *yapısından* doğan bir kısıtı (kod geç oluştuğu için dinamik test geç) doğru tarif eder; (c) ise doğru aktörü (geliştirici) yakalayıp yanlış yürütme biçimini (manuel) iddia eder — döngüsel modelde bileşen testi otomasyona dayanır.

**Yanılgı etiketi:** `ygyd-modeli-test-zamanlamasi-eslestirmesi`

---
### B-10 · FL-2.1.2 · K1
**Senin cevabın:** a · **Doğru cevap:** b

**Neyi soruyor:** Seçilen YGYD modelinden bağımsız olarak her modelde geçerli olan iyi test uygulamalarından birini, özellikle test uzmanlarının gözden geçirmeye ne zaman katılması gerektiğini soruyor.

**Doğru şık neden doğru:** Syllabus, model bağımsız iyi uygulamalar listesinde gözden geçirmeye katılım zamanını "taslaklar hazır olur olmaz" diye tanımlar.
> ALINTI: "Test uzmanları, iş ürünlerinin taslakları hazır olur olmaz iş ürünlerini gözden geçirme sürecine"

Devamında bunun gerekçesi erken test ve shift-left'tir: iş ürünü henüz taslak halindeyken gözden geçirilirse hatalar en ucuz noktada yakalanır.

**Senin şıkkın neden yanlış:** (a) "Çalışma ürünlerini bir sonraki geliştirme aşamasının bir parçası olarak gözden geçirmek" — bu, sıralı/aşamalı modellerdeki *aşama kapısı (phase gate)* mantığını tarif eder: iş ürünü tamamlanır, aşama biter, sonraki aşamada gözden geçirilir. Bu tam olarak shift-left'in tersidir ve geri bildirimi bir aşama geciktirir. Ayrıca "bir sonraki geliştirme aşaması" kavramı yalnızca sıralı modellerde anlamlıdır, dolayısıyla "tüm YGYD modelleri için geçerli" koşulunu da sağlamaz.

Diğer çeldiriciler: (c) gözden geçirmeyi test analizi/tasarımına bağlar, oysa syllabus'un ölçütü taslağın hazır olmasıdır; (d) "yayınlandıktan hemen sonra" daha da geç bir noktadır.

**Ayırt edici fark:** Doğru ölçüt iş ürününün *taslak* haline gelmesidir (erken test/shift-left); senin şıkkın ise iş ürününün *tamamlanıp bir sonraki aşamaya geçmesini* bekler.

**Yanılgı etiketi:** `gozden-gecirme-zamanlamasi-tamamlanmayi-bekleme`

---
### B-13 · FL-2.2.1 · K2
**Senin cevabın:** d · **Doğru cevap:** a

**Neyi soruyor:** Dört test senaryosundan hangisinin **sistem testi** seviyesinde yapılma olasılığının en yüksek olduğunu soruyor. Her çeldirici farklı bir test seviyesine ait.

**Doğru şık neden doğru:** Sistem testi, sistemin bütün olarak davranışına odaklanır, fonksiyonel olmayan test çeşitlerini (güvenlik dahil) kapsar ve tipik olarak bağımsız bir test ekibi tarafından yürütülür.
> ALINTI: "Sistem testi bir sistemin veya ürünün genel davranışına ve yeteneklerine odaklanır, genellikle"

> ALINTI: "Sistem testi bağımsız bir test ekibi tarafından"

(a) şıkkındaki üç işaret de bu tanımla örtüşür: komple bir sistem (kredi yönetim sistemi), fonksiyonel olmayan bir kalite karakteristiği (güvenlik) ve bağımsız test ekibi.

**Senin şıkkın neden yanlış:** (d) "Kullanıcı arayüzü ile veri tabanı arasındaki etkileşimlerin test edilmesi" — bu, sistemin *içindeki* iki bileşen arasındaki arayüz ve etkileşimin testidir, yani **bileşen entegrasyon testi**dir.
> ALINTI: "Bileşen entegrasyon testi (birim entegrasyon testi olarak da bilinir) arayüzlerin ve bileşenler"

> ALINTI: "arasındaki etkileşimlerin testine odaklanır."

Sistem testi ise tek tek bileşen çiftlerinin arayüzüne değil, sistemin uçtan uca genel davranışına bakar.

Diğer çeldiriciler: (b) harici bankacılık sistemiyle arayüz = **sistem entegrasyon testi**:
> ALINTI: "Sistem entegrasyon testi test edilen sistem ile diğer sistemler ve harici hizmetler arasındaki"

(c) beta testi = **kabul testi** çeşidi:
> ALINTI: "kabul testi ve düzenleyici kabul testi, alfa testi ve beta testi."

**Ayırt edici fark:** Sistem testi *tek bir komple sistemin bütünsel davranışını* test eder; senin seçtiğin şık ise *aynı sistemin iki iç bileşeni arasındaki arayüzü* test eder — bu bileşen entegrasyon testidir.

**Yanılgı etiketi:** `test-seviyesi-ayrimi-entegrasyon-vs-sistem`

---
### D-9 · FL-2.1.2 · K1
**Senin cevabın:** d · **Doğru cevap:** a

**Neyi soruyor:** Tüm YGYD modellerine uygulanabilen iyi test uygulamalarından hangisinin doğru ifade edildiğini soruyor (B-10 ile aynı syllabus maddesi listesi, farklı maddeleri sınıyor).

**Doğru şık neden doğru:** Model bağımsız iyi uygulamalar listesinde, her test seviyesinin kendine özgü hedefleri olduğu doğrudan yer alır; bunun amacı hem yeterli kapsam sağlamak hem de seviyeler arası gereksiz tekrarı önlemektir.
> ALINTI: "Farklı test seviyeleri (bkz. konu 2.2.1) belirli ve farklı test hedeflerine sahiptir ve bu da testin"

**Senin şıkkın neden yanlış:** (d) "Her dinamik test faaliyetinin karşılık gelen bir statik test faaliyeti vardır." Bu ifade, syllabus'taki gerçek maddenin çarpıtılmış halidir. Syllabus'un kurduğu eşleme **geliştirme faaliyeti ↔ test faaliyeti** arasındadır, **dinamik test ↔ statik test** arasında değildir.
> ALINTI: "Her yazılım geliştirme faaliyetine karşılık gelen bir test faaliyeti vardır ve böylece tüm"

Yani her geliştirme faaliyetinin kalite kontrolüne tabi olması gerekir; ancak bir dinamik testin her zaman kendisine karşılık gelen bir statik testi olması diye bir kural yoktur.

Diğer çeldiriciler: (b) yanlıştır çünkü ilgili geliştirme aşamasında başlaması gereken şey testin *uygulanması ve yürütülmesi* değil, **test analizi ve tasarımı**dır:
> ALINTI: "Belirli bir test seviyesi için test analizi ve tasarımı YGYD’nin ilgili geliştirme aşamasında başlar"

(c) yanlıştır çünkü taslaklar hazır olur olmaz başlaması gereken faaliyet test tasarımı değil, iş ürünlerinin **gözden geçirilmesi**dir (bkz. B-10).

**Ayırt edici fark:** Syllabus'un eşleme ekseni "geliştirme faaliyeti → test faaliyeti"dir; senin şıkkın bu ekseni "dinamik test → statik test" olarak değiştirerek syllabus'ta olmayan bir kural uydurur.

**Yanılgı etiketi:** `syllabus-maddesinin-ekseni-kaydirilmis-celdirici`

---
### D-10 · FL-2.1.3 · K1
**Senin cevabın:** b · **Doğru cevap:** a

**Neyi soruyor:** "Önce test et" (test-first) yaklaşımının gerçek bir örneğinin hangi şıkta verildiğini soruyor. Şıklardan üçü uydurma "X Güdümlü Geliştirme" isimleridir.

**Doğru şık neden doğru:** Syllabus test-first yaklaşımları olarak yalnızca TDD, ATDD ve BDD'yi tanımlar; ortak özellikleri testlerin koddan önce tanımlanmasıdır.
> ALINTI: "yaklaşımını izler (bkz. bölüm 2.1.5), çünkü testler kod yazılmadan önce tanımlanır."

BDD bu üçlünün içinde açıkça başlık olarak yer alır:
> ALINTI: "Davranış Güdümlü Yazılım Geliştirme (BDD):"

Dolayısıyla (a) Davranış Güdümlü Yazılım Geliştirme doğru cevaptır.

**Senin şıkkın neden yanlış:** (b) "Test Düzeyi Güdümlü Yazılım Geliştirme" diye bir yaklaşım syllabus'ta (ve sektörde) yoktur. Adındaki "Test" ve "Güdümlü" kelimeleri, "Test Güdümlü Yazılım Geliştirme"yi (TDD) çağrıştırdığı için tuzak olarak konmuştur; ama araya sokulan "Düzeyi/Seviyesi" kelimesi terimi geçersiz kılar. Şıkta gerçek TDD olsaydı o da doğru olurdu; ancak listelenen tek geçerli test-first yaklaşımı BDD'dir.

Aynı şekilde (c) "Fonksiyon Güdümlü" (syllabus'ta geçen terim *özellik güdümlü geliştirme / FDD*'dir ve o da bir test-first yaklaşımı değil, bir Çevik geliştirme yöntemidir) ve (d) "Performans Güdümlü" de uydurma isimlerdir.

**Ayırt edici fark:** Test-first kümesi syllabus'ta tam olarak üç elemanlıdır — TDD, ATDD, BDD; senin seçtiğin isim bu kümede yer almayan, TDD'ye benzetilerek türetilmiş sahte bir terimdir.

**Yanılgı etiketi:** `benzer-isimli-sahte-terim-secimi`

---
### D-11 · FL-2.1.4 · K2
**Senin cevabın:** b · **Doğru cevap:** d

**Neyi soruyor:** DevOps uygulanırken karşılaşılması EN OLASI zorluğun/riskin hangisi olduğunu soruyor. Syllabus'un "DevOps'un risk ve zorlukları" listesine doğrudan dayanan bir soru.

**Doğru şık neden doğru:** Syllabus'un DevOps riskleri listesi hem teslimat hattının kurulması hem de test otomasyonunun kurulup sürdürülmesinin zorluğunu ayrı ayrı sayar; (d) şıkkı bu iki maddeyi tek cümlede birleştirir.
> ALINTI: "DevOps teslimat hattı tanımlanmalı ve kurulmalıdır"

> ALINTI: "Test otomasyonu ek kaynaklar gerektirir. Test otomasyonunun kurması ve sürdürmesi zor olabilir"

**Senin şıkkın neden yanlış:** (b) "Sürekli değişen test ortamlarını yönetmek" — bu, DevOps'un bir *zorluğu* değil, tam tersine çözdüğü bir sorundur. Syllabus, DevOps'un faydaları arasında CI/CD sayesinde ortamların **stabil** hale gelmesini sayar:
> ALINTI: "Stabil test ortamları oluşturmayı kolaylaştıran CI/CD gibi otomatik süreçleri destekler"

Yani senin seçtiğin ifade, DevOps'suz (manuel ortam kurulumlu) bir dünyanın sorununu tarif eder; DevOps riskleri listesinde yer almaz.

Diğer çeldiriciler de aynı şekilde "fayda"nın zorluk gibi sunulmuş halidir: (a) fonksiyonel olmayan karakteristiklerin gözden kaçmaması DevOps'un bir faydasıdır —
> ALINTI: "Fonksiyonel olmayan kalite karakteristiklerine (ör. performans verimliliği ve güvenilirlik) ilişkin"

— görünürlüğü artırır. (c) ise yanlıştır çünkü DevOps manuel test ihtiyacını *azaltır*, artırmaz; manuel test tamamen ortadan kalkmaz ama "daha fazla manuel test uzmanına ihtiyaç" doğmaz:
> ALINTI: "Her ne kadar DevOps kapsamında yüksek düzeyde test otomasyonu bulunsa da özellikle kullanıcı"

**Ayırt edici fark:** Doğru şık DevOps'u *kurmanın* maliyetini (pipeline + otomasyon altyapısı) anlatır; senin şıkkın ise DevOps'un ortadan kaldırdığı bir sorunu (kararsız test ortamları) zorluk sanır.

**Yanılgı etiketi:** `devops-fayda-risk-listesi-karistirma`

---

## Yanılgı Etiketi Özeti

| Etiket | Sorular |
|---|---|
| `shift-left-kapsam-yanlis-genisletme` | A-11 |
| `ygyd-modeli-test-zamanlamasi-eslestirmesi` | B-9 |
| `gozden-gecirme-zamanlamasi-tamamlanmayi-bekleme` | B-10 |
| `test-seviyesi-ayrimi-entegrasyon-vs-sistem` | B-13 |
| `syllabus-maddesinin-ekseni-kaydirilmis-celdirici` | D-9 |
| `benzer-isimli-sahte-terim-secimi` | D-10 |
| `devops-fayda-risk-listesi-karistirma` | D-11 |

**Üst-düzey örüntü:** 7 yanlışın 5'i (A-11, B-10, B-9, D-9, D-11) syllabus'ta **madde madde listelenmiş** bölümlerden geliyor (2.1.2 iyi uygulamalar listesi, 2.1.4 DevOps fayda/risk listeleri, 2.1.5 shift-left iyi uygulamalar listesi). Çeldiriciler tipik olarak listedeki bir maddenin *bir kelimesini* değiştirerek (taslak→tamamlanmış, test analizi→test yürütme, geliştirme faaliyeti→dinamik test) veya fayda listesindeki maddeyi risk listesine taşıyarak üretiliyor. Bu üç listeyi ezberden değil, madde madde ayırt ederek çalışmak en yüksek getirili tekrar alanı.

## Bölüm 3 — Statik Test  (7 soru)

### A-15 · FL-3.1.2 · K2
**Senin cevabın:** b · **Doğru cevap:** a

**Neyi soruyor:** Statik testin syllabus'ta sayılan faydalarından hangisinin GERÇEK bir fayda OLMADIĞINI soruyor. Yani üç şık gerçek fayda, biri çarpıtılmış ifade.

**Doğru şık neden doğru:** (a) şıkkı statik testin faydasını "hataların YGYD'nin **ilerleyen** aşamalarında tespit edilmesini kolaylaştırması" diye tarif ediyor. Bu, syllabus'un söylediğinin tam tersidir: statik testin değeri hataları **erken** aşamada yakalamasıdır.
> ALINTI: "Statik test YGYD'nin erken aşamalarında hataları tespit ederek erken test prensibini yerine getirebilir"

Ayrıca maliyet mantığı da tersine çevrilmiş: hata ilerleyen aşamada bulunursa maliyet artar, azalmaz.
> ALINTI: "Çünkü projenin ilerleyen aşamalarında hataları"

**Senin şıkkın neden yanlış:** (b) şıkkı — statik testte bulunan hataları düzeltmenin dinamik testte bulunanlara göre daha ucuz olması — syllabus'un gözden geçirmelere yapılan yatırımın yüksek geri dönüşü argümanının birebir karşılığıdır, yani **gerçek bir faydadır**. Soru "DEĞİLDİR" dediği için gerçek faydayı işaretlemek hatalıdır.

**Ayırt edici fark:** (a) hatanın "geç" bulunmasını fayda diye sunarak erken test prensibini tersine çevirir; (b), (c), (d) ise syllabus'ta açıkça sayılan gerçek statik test faydalarıdır.

**Yanılgı etiketi:** `degildir-sorusunda-dogru-ifadeyi-isaretleme`

---
### A-16 · FL-3.2.1 · K1
**Senin cevabın:** b · **Doğru cevap:** d

**Neyi soruyor:** Erken ve sık paydaş geri bildiriminin syllabus'ta (3.2.1) sayılan faydalarından birini soruyor.

**Doğru şık neden doğru:** (d) "Gereksinimler konusunda yanlış anlaşılmaları önlemeye yardımcı olur" ifadesi syllabus 3.2.1'deki cümlenin doğrudan karşılığıdır.
> ALINTI: "YGYD boyunca sıkça verilen paydaş geri bildirimleri gereksinimler hakkındaki yanlış anlaşılmaları"

(Devamı: "önleyebilir ve gereksinimlerdeki değişikliklerin daha erken anlaşılmasını ve uygulanmasını sağlayabilir.")

**Senin şıkkın neden yanlış:** (b) "Müşterilerin, üzerinde anlaşılan risklere göre gereksinimleri önceliklendirmelerini sağlar" ifadesi syllabus'taki risk cümlesinin çarpıtılmış halidir. Syllabus, geri bildirimin **geliştirme ekibinin/paydaşların en çok değer katan ve riskler üzerinde en olumlu etkiyi yapan özelliklere odaklanmasını** sağladığını söyler — "müşterinin gereksinim önceliklendirmesi" farklı bir faaliyettir (risk bazlı test/ürün iş listesi önceliklendirmesi, bölüm 5.2 alanı).
> ALINTI: "Paydaşlara en çok değer"

**Ayırt edici fark:** Doğru şık geri bildirimin **iletişim/anlayış** faydasını (yanlış anlaşılmaların önlenmesi) söyler; senin şıkkın ise geri bildirimin faydası değil, ayrı bir **risk bazlı önceliklendirme** faaliyetini tarif eder.

**Yanılgı etiketi:** `syllabus-ifadesinin-carpitilmis-versiyonunu-secme`

---
### A-17 · FL-3.2.4 · K2
**Senin cevabın:** d · **Doğru cevap:** b

**Neyi soruyor:** Verilen özellik listesinden (katip var, amaç kaliteyi değerlendirmek, toplantıyı **yazar** yönetiyor, bireysel hazırlık var, rapor üretiliyor) hangi gözden geçirme çeşidinin kullanıldığını soruyor.

**Doğru şık neden doğru:** Belirleyici ipucu "gözden geçirme toplantıları **çalışma ürününün yazarı tarafından yönetilir**"dir. Yazarın öncülüğünde yürüyen tek gözden geçirme çeşidi Üzerinden geçmedir (walkthrough) ve amacı arasında kaliteyi değerlendirmek açıkça sayılır.
> ALINTI: "Üzerinden geçme. Yazarın öncülüğündeki bir üzerinden geçme süreci kaliteyi değerlendirmek"

"Bireysel hazırlık vardır" ifadesi de üzerinden geçmeyle çelişmez; syllabus bunu opsiyonel bırakır:
> ALINTI: "geçiriciler, üzerinden geçme süreci öncesinde bireysel gözden geçirme yapabilir ancak bu"

**Senin şıkkın neden yanlış:** (d) Teftiş (Inspection) en resmi gözden geçirme çeşididir; ana hedefi kaliteyi değerlendirmek değil **maksimum sayıda anomali bulmaktır** ve teftişte yazar toplantıyı yönetemez.
> ALINTI: "eksiksiz olarak izlenir (bkz. bölüm 3.2.2). Ana hedef maksimum sayıda anomali bulmaktır."
> ALINTI: "gözden geçirme lideri veya katip olarak görev yapamaz."

**Ayırt edici fark:** Toplantıyı **yazarın** yönetmesi üzerinden geçmenin imzasıdır; teftişte yazarın gözden geçirme lideri/katip olması yasaktır ve ana hedef anomali sayısını maksimize etmektir.

**Yanılgı etiketi:** `gozden-gecirme-turleri-karisikligi`

---
### A-18 · FL-3.2.5 · K1
**Senin cevabın:** c · **Doğru cevap:** d

**Neyi soruyor:** Başarılı gözden geçirmeye katkıda bulunan faktörlerden hangisinin faktör OLMADIĞINI soruyor.

**Doğru şık neden doğru:** (d) "Bulunan hatalar **hiç koşulsuz** kabul edilmeli, takdir edilmeli ve nesnel olarak ele alınmalıdır" ifadesindeki "hiç koşulsuz kabul" kısmı syllabus'la doğrudan çelişir. Syllabus, gözden geçirmede bulunan anomalilerin koşulsuz kabul edilmesini değil, **analiz edilip tartışılmasını** şart koşar; çünkü her anomali hata değildir.
> ALINTI: "gerekmediğinden, tüm bu anomalilerin analiz edilmesi ve tartışılması gerekir."

**Senin şıkkın neden yanlış:** (c) "Katılımcılar diğer katılımcılara karşı negatif davranışlardan kaçınmalıdır" ifadesi, gözden geçirmenin insan/kültür boyutuna ait bir başarı faktörüdür (moderatörün "herkesin özgürce" konuşabileceği güvenli bir ortam sağlaması ve "gözden geçirmelerin şirket kültürünün bir parçası" olması maddeleriyle aynı çizgide). Yani gerçek bir başarı faktörüdür, dolayısıyla "DEĞİLDİR" sorusunda seçilmemeliydi.
> KAYNAK YOK: syllabus'ta doğrudan karşılık bulunamadı (Türkçe metindeki 3.2.5 madde listesinde bu cümle birebir yer almıyor; ancak 3.2.3'teki moderatör tanımı ve 3.2.5'teki kültür maddesi bu faktörü destekler)

Not: (a) ve (b) şıkları da syllabus'ta birebir başarı faktörüdür:
> ALINTI: "Gözden geçirmeye hazırlanmaları için katılımcılara yeterli sürenin verilmesi"
> ALINTI: "toplantısı sırasında konsantrasyonlarını kaybetmesinler diye gözden geçirmelerin küçük"

**Ayırt edici fark:** (c) davranışsal bir başarı faktörüdür; (d) ise "hiç koşulsuz kabul" diyerek anomalilerin analiz ve tartışma zorunluluğunu ortadan kaldırdığı için başarı faktörü değil, sürece aykırı bir ifadedir.

**Yanılgı etiketi:** `degildir-sorusunda-dogru-ifadeyi-isaretleme`

---
### B-17 · FL-3.2.2 · K2
**Senin cevabın:** c · **Doğru cevap:** d

**Neyi soruyor:** Dört görev tanımının gözden geçirme süreci faaliyetleriyle (Planlama, Başlatma, Bireysel gözden geçirme, İletişim ve analiz) eşleşmesini soruyor.

**Doğru şık neden doğru:** Doğru eşleme **1C, 2B, 3A, 4D** (şık d):
- **1 → C (Planlama):** kalite karakteristiği ve çıkış kriterlerinin belirlenmesi planlama faaliyetidir.
> ALINTI: "kalite karakteristiği, odaklanılacak alanlar, çıkış kriterleri, standartlar, efor gibi destekleyici bilgiler"
- **2 → B (Gözden geçirmeyi başlatma):** herkesin çalışma ürününe erişiminin sağlanması başlatma faaliyetidir.
> ALINTI: "geçirilen çalışma ürününe erişebilmesini, rollerini ve sorumluluklarını anlamasını ve gözden"
- **3 → A (Bireysel gözden geçirme):** anormalliklerin tespit edilmesi bireysel gözden geçirmede olur.
> ALINTI: "belirlemek için bireysel bir gözden geçirme yapar"
- **4 → D (İletişim ve analiz):** anomalilerin tartışılması bu faaliyettedir.
> ALINTI: "gerekmediğinden, tüm bu anomalilerin analiz edilmesi ve tartışılması gerekir."

**Senin şıkkın neden yanlış:** (c) = 1C, 2A, 3B, 4D. **1 ve 4'ü doğru yapmışsın**; hatan yalnızca 2 ile 3'ün yer değiştirmesi: "herkesin çalışma ürününe erişimi var" ifadesini Bireysel gözden geçirmeye, "anormallikler tespit edilir" ifadesini Başlatmaya bağlamışsın. Erişimin sağlanması bir **hazırlık/erişim** işidir (başlatma); anomali **tespiti** ise gözden geçiricinin fiilen ürünü incelediği bireysel gözden geçirmede gerçekleşir.

**Ayırt edici fark:** Başlatma = herkesi ve her şeyi hazır hale getirmek (erişim, roller); Bireysel gözden geçirme = ürünü fiilen inceleyip anomalileri/soruları belirlemek.

**Yanılgı etiketi:** `gozden-gecirme-sureci-faaliyet-sirasi-karisikligi`

---
### C-17 · FL-3.2.4 · K2
**Senin cevabın:** d · **Doğru cevap:** b

**Neyi soruyor:** Dört gözden geçirme çeşidinin (teknik, gayri resmi, teftiş, üzerinden geçme) hedef/özellik açıklamalarıyla eşleşmesini soruyor.

**Doğru şık neden doğru:** Doğru eşleme **1A, 2D, 3C, 4B** (şık b):
- **1 Teknik gözden geçirme → A** (fikir birliği, yeni fikirler, yazarı iyileştirmeye teşvik):
> ALINTI: "amaçları arasında teknik bir problemle ilgili fikir birliği sağlamak ve buna ilişkin karar almak,"
- **2 Gayri resmi → D** (ana hedef anomali tespiti, resmi dokümante çıktı YOK):
> ALINTI: "izlenmez ve bunlar resmi olarak belgelenmiş bir çıktı gerektirmez. Ana hedef anomalileri"
- **3 Teftiş → C** (ana hedef anomali tespiti + süreç iyileştirme için metrik toplama):
> ALINTI: "toplanır ve teftiş süreci de dahil olmak üzere YGYD"
- **4 Üzerinden geçme → B** (gözden geçiricileri eğitmek, fikir birliği, yeni fikirler, anomali tespiti):
> ALINTI: "ve çalışma ürününe yönelik güven oluşturmak, gözden geçiricileri eğitmek, fikir birliğine"

**Senin şıkkın neden yanlış:** (d) = 1C, 2D, 3A, 4B. **2 ve 4'ü doğru yapmışsın** (gayri resmi → D, üzerinden geçme → B); hatan 1 ile 3'ü takas etmen: Teknik gözden geçirmeye **C** (metrik toplayan, süreç iyileştirmeyi destekleyen) açıklamasını, Teftişe ise **A** (fikir birliği/yeni fikir/yazarı motive etme) açıklamasını vermişsin. Metrik toplama ve süreç iyileştirme yalnızca **teftişin** ayırt edici özelliğidir; teknik gözden geçirmenin syllabus'ta metrik toplama zorunluluğu yoktur.

**Ayırt edici fark:** Teftiş = en resmi çeşit, ana hedef maksimum anomali + YGYD iyileştirmesi için **metrik toplama**; Teknik gözden geçirme = teknik açıdan nitelikli gözden geçiricilerin, **moderatör** yönetiminde teknik konuda **fikir birliğine varması**, metrik zorunluluğu yok.

**Yanılgı etiketi:** `gozden-gecirme-turleri-karisikligi`

---
### D-16 · FL-3.1.2 · K2
**Senin cevabın:** a · **Doğru cevap:** c

**Neyi soruyor:** Statik testin değeri hakkında — statik testle bulunabilen hata kümesi ile dinamik testle bulunabilen hata kümesinin ilişkisini soruyor.

**Doğru şık neden doğru:** (c) "Dinamik test, statik testle bulunabilecek hataların bir kısmını belirleyebilir, ancak hepsini belirleyemez." İki kümenin **kesişimi vardır ama dinamik test statik testin bulduklarının tamamını kapsamaz**; statik testin dinamik testle asla bulunamayacak hataları vardır.
> ALINTI: "Ayrıca, dinamik testle tespit edilemeyecek hataları da bulabilir"
> ALINTI: "ancak bazı hata çeşitleri ya statik testle ya da dinamik testle bulunabilir."

Buradaki "ya ... ya da" ifadesi, bazı hata çeşitlerinin yalnızca bir tarafla bulunabildiğini; geri kalanların ise her ikisiyle de bulunabildiğini söyler — yani kısmi örtüşme.

**Senin şıkkın neden yanlış:** (a) "Statik testle bulunan hata türleri, dinamik testle bulunabilecek hata türlerinden farklıdır" ifadesi, iki kümenin **tamamen ayrık** (hiç kesişmeyen) olduğunu iddia eder. Syllabus ise ikisinin birbirini **tamamladığını** ve **benzer hedeflere** sahip olduğunu, dolayısıyla ortak bulunabilen hata çeşitleri olduğunu söyler ("Statik test ve dinamik testler birbirlerini tamamlar."). Senin şıkkın syllabus'un "bazı hata çeşitleri" nüansını "tüm hata çeşitleri" haline getiriyor.

**Ayırt edici fark:** Doğru şık **kısmi örtüşme** (dinamik test statik testin bulduklarının bir kısmını yakalar) der; senin şıkkın ise **tam ayrıklık** (hiç örtüşme yok) iddia eder — syllabus kısmi örtüşmeyi savunur.

**Yanılgı etiketi:** `statik-dinamik-hata-kumesi-ortusmesi`

---

## Tekrar Eden Yanılgı Etiketleri (özet)

| Etiket | Sorular | Sayı |
|---|---|---|
| `gozden-gecirme-turleri-karisikligi` | A-17, C-17 | 2 |
| `degildir-sorusunda-dogru-ifadeyi-isaretleme` | A-15, A-18 | 2 |
| `gozden-gecirme-sureci-faaliyet-sirasi-karisikligi` | B-17 | 1 |
| `syllabus-ifadesinin-carpitilmis-versiyonunu-secme` | A-16 | 1 |
| `statik-dinamik-hata-kumesi-ortusmesi` | D-16 | 1 |

## Bölüm 4 — Kara Kutu Test Teknikleri  (10 soru)

### A-20 · FL-4.2.1 · K3
**Senin cevabın:** c (5) · **Doğru cevap:** b (4)

**Neyi soruyor:** İki pay grubu (kat ve bahçe tipi) olan bir formda, geçersiz kombinasyonların doğrulama ile engellendiği durumda %100 denklik payı (Each Choice) kapsamı için gereken MİNİMUM test senaryosu sayısı.

**Doğru şık neden doğru:**
Adım adım türetme:
1. Pay grubu 1 — kat: {zemin kat}, {birinci kat}, {ikinci kat+} → 3 pay.
2. Pay grubu 2 — bahçe tipi: {bahçesiz}, {küçük bahçe}, {büyük bahçe} → 3 pay.
3. Toplam 6 pay var; her test senaryosu bir kat payı + bir bahçe payı kapsar, yani bir testte aynı anda 2 pay örtülür.
4. Kural kısıtı: yalnızca zemin kat bahçeli olabilir. Yani "küçük bahçe" ve "büyük bahçe" payları SADECE zemin kat ile eşleşebilir. "Birinci kat" ve "ikinci kat+" ise sadece "bahçesiz" ile eşleşebilir.
5. Zorunlu testler:
   - T1: zemin kat + küçük bahçe (küçük bahçe payını kapsayan tek yol)
   - T2: zemin kat + büyük bahçe (büyük bahçe payını kapsayan tek yol)
   - T3: birinci kat + bahçesiz
   - T4: ikinci kat+ + bahçesiz
6. Kontrol: kat payları {zemin (T1,T2), birinci (T3), ikinci+ (T4)} = 3/3 ✔; bahçe payları {küçük (T1), büyük (T2), bahçesiz (T3,T4)} = 3/3 ✔. 6/6 pay kapsandı → %100.
7. "zemin kat + bahçesiz" testine gerek YOKTUR, çünkü her iki payı da T1–T4 zaten kapsıyor. Dolayısıyla minimum = **4**.

> ALINTI: "Each Choice kapsamı, test senaryolarının her pay grubundan her bir payı"
> ALINTI: "en az bir kez denemesini gerektirir. Each Choice kapsamı pay kombinasyonlarını dikkate almaz."
> ALINTI: "Dolayısıyla her pay için bir test yapılması yeterlidir."

**Senin şıkkın neden yanlış:** 5 rakamı, "zemin kat"ı üç bahçe tipiyle de ayrı ayrı test etme (3 test) + birinci kat ve ikinci kat+ için birer test (2 test) = 5 hesabından çıkar. Ancak "zemin kat + bahçesiz" testi hiçbir YENİ pay eklemez: zemin kat payı zaten diğer iki testte, bahçesiz payı zaten birinci/ikinci kat testlerinde kapsanmıştır. Bu, Each Choice yerine farkında olmadan kombinasyon kapsamına doğru kayma hatasıdır.

**Ayırt edici fark:** Each Choice kapsamı her payın en az bir kez denenmesini ister, pay KOMBİNASYONLARININ denenmesini değil; bu yüzden zaten kapsanmış iki payı tekrar birleştiren 5. test kapsamı artırmaz.

**Yanılgı etiketi:** `each-choice-yerine-kombinasyon-sayma`

---
### A-21 · FL-4.2.2 · K3
**Senin cevabın:** d (%100) · **Doğru cevap:** a (%50)

**Neyi soruyor:** 6 not aralığı için verilmiş 6 test senaryosunun ulaştığı 2-değerli Sınır Değer Analizi (SDA/BVA) kapsam yüzdesi.

**Doğru şık neden doğru:**
Not: Paket metninde tablonun girdi sütunu kaybolmuştu; `raw/SinavA.txt` (satır 989–1010) üzerinden girdiler kurtarıldı: TC1=91, TC2=50, TC3=81, TC4=60, TC5=70, TC6=80.

Adım adım türetme:
1. Paylar (6 adet): [0–50], [51–60], [61–70], [71–80], [81–90], [91–100].
2. Her payın min ve max değeri o payın sınır değeridir → toplam sınır değer sayısı = 6 pay × 2 = **12**:
   0, 50 | 51, 60 | 61, 70 | 71, 80 | 81, 90 | 91, 100.
3. 2-değerli SDA'da kapsam öğeleri tanımlanan tüm sınır değerlerdir (sınır değer + bitişik paydaki en yakın komşusu; bu çiftler zaten yukarıdaki 12 değerin içindedir).
4. Test setinin dendiği değerler: 91, 50, 81, 60, 70, 80 → hepsi sınır değerdir, 6 farklı kapsam öğesi.
5. Kapsam = denenen sınır değer / toplam sınır değer = 6 / 12 = **%50**.

> ALINTI: "SDA sadece sıralı verilerden oluşan paylarda kullanılabilir. Bir payın minimum ve maksimum değerleri o"
> ALINTI: "değer ve bitişik paya ait en yakın komşusu. 2 değerli SDA ile %100 kapsama ulaşmak için test"
> ALINTI: "Kapsam, test senaryolarında denenen sınır değerlerin sayısının tanımlanan tüm sınır değerlerin"

**Senin şıkkın neden yanlış:** %100, "6 payın 6'sı da bir sonuç üretti, hepsi kapsandı" akıl yürütmesinden çıkar — bu DPA (denklik payı) kapsamıdır, SDA kapsamı değil. SDA'da kapsam öğesi PAY değil, SINIR DEĞERdir; her payın iki sınırı vardır ve testler her paydan yalnızca birer sınırı denemiştir (ör. [0–50] payında 50 denendi ama 0 denenmedi; [91–100] payında 91 denendi ama 100 denenmedi).

**Ayırt edici fark:** DPA kapsamı payları sayar (6/6 = %100), 2-değerli SDA kapsamı sınır değerleri sayar (6/12 = %50); soru SDA kapsamını soruyor.

**Yanılgı etiketi:** `sda-kapsamini-dpa-kapsami-sanma`

---
### B-19 · FL-4.1.1 · K2
**Senin cevabın:** a · **Doğru cevap:** d

**Neyi soruyor:** Karar tablosu testi (kara kutu) ile dal testi (beyaz kutu) arasındaki temel farkı en iyi ifade eden cümle.

**Doğru şık neden doğru:** Karar tablosu testi bir KARA KUTU tekniğidir: iş kurallarını tanımlayan spesifikasyondan türetilir ve yazılımın nasıl uygulandığından bağımsızdır. Dal testi ise bir BEYAZ KUTU tekniğidir: kontrol akış grafiğine dayandığı için ancak kod tasarlandıktan/yazıldıktan sonra oluşturulabilir. d şıkkı tam olarak bu iki cümleyi söyler.

> ALINTI: "Kara kutu test teknikleri (spesifikasyon bazlı teknikler olarak da bilinir) test nesnesinin iç yapısına atıfta"
> ALINTI: "yazılımın nasıl yazıldığından bağımsızdır. Sonuç olarak, kod değişir ancak test nesnesinin davranışı aynı"
> ALINTI: "analizine dayanır. Test senaryoları yazılımın nasıl tasarlandığına bağlı olduğundan sadece test"
> ALINTI: "nesnesinin tasarımı veya kodlanmasından sonra oluşturulabilir."
> ALINTI: "Dal, test nesnesinde komutların çalıştırıldığı olası sıraları gösteren kontrol akış grafiğindeki iki düğüm"

**Senin şıkkın neden yanlış:** a şıkkı "karar tablosu testinde test senaryoları KODDAKİ karar ifadelerinden türetilir" diyor — bu karar tablosunu beyaz kutu tekniği yapar ve yanlıştır. Karar tablosundaki "koşullar" koddaki `if` ifadeleri değil, spesifikasyondaki iş kurallarıdır. a'nın ikinci yarısı (dal testi = kontrol akışı) doğru, ama birinci yarısı yanlış olduğu için şık tümüyle yanlıştır. (Not: c şıkkı da aynı ikiliyi tersine çevirmiş hâlidir.)

**Ayırt edici fark:** Karar tablosunun kaynağı SPESİFİKASYONDAKİ iş kurallarıdır (koddan bağımsız), dal testinin kaynağı KODUN kontrol akış grafiğidir (kod olmadan üretilemez).

**Yanılgı etiketi:** `karar-tablosunu-beyaz-kutu-sanma`

---
### B-20 · FL-4.2.1 · K3
**Senin cevabın:** c (1, 10, 50) · **Doğru cevap:** a (19, 20, 30)

**Neyi soruyor:** İndirim kurallarına göre oluşan denklik paylarını en yüksek oranda kapsayan test verisi setini seçmek.

**Doğru şık neden doğru:**
Adım adım türetme:
1. Kuraldan çıkan paylar (çıktı/davranış temelli, 3 pay):
   - P1 — indirim yok: 10'un katı olmayan yıkama sayıları.
   - P2 — %10 indirim: 10'un katı olan ama 20'nin katı OLMAYAN sayılar (10, 30, 50, 70, 90…).
   - P3 — %50 indirim (10 + 40): 20'nin katı olan sayılar (20, 40, 60…).
2. Şıkların pay eşlemesi:
   - a) 19 → P1; 20 → P3; 30 → P2 ⇒ **3/3 pay = %100**
   - b) 11 → P1; 12 → P1; 20 → P3 ⇒ 2/3
   - c) 1 → P1; 10 → P2; 50 → P2 (50/10 = 5 tam, 50/20 = 2,5 → 20'nin katı DEĞİL) ⇒ 2/3
   - d) 10 → P2; 29 → P1; 30 → P2; 31 → P1 ⇒ 2/3
3. En yüksek kapsam a şıkkında (%100).

> ALINTI: "DPA'da kapsam öğeleri denklik paylarıdır. Bu teknikle kapsamın %100'üne ulaşmak için test senaryoları,"
> ALINTI: "her payı en az bir kez kapsama alarak, belirlenmiş tüm payları (geçersiz paylar dahil) denemesi"
> ALINTI: "Kapsam, denenen payların sayısının, tanımlanan payların toplam sayısına bölünmesiyle"

**Senin şıkkın neden yanlış:** c şıkkını seçmek büyük olasılıkla 50 sayısını "%50 indirim" payına atamaktan kaynaklanıyor (50 sayısı ile %50 indirim yüzdesinin karıştırılması) veya 50'nin 20'nin katı olduğunu varsaymaktan. Oysa %50 indirim payına düşmek için sayının 20'ye tam bölünmesi gerekir; 50 sadece 10'un katıdır → 10 ile aynı paya (P2) düşer. Sonuç: c şıkkında 3 test iki paya dağılır, üçüncü pay hiç denenmez.

**Ayırt edici fark:** Payı belirleyen şey sayının kendisi değil, sayının hangi indirim davranışını tetiklediğidir; 50 ile 10 aynı paydadır (yalnızca %10 indirim), 20 ise ayrı bir paydadır (%50 indirim).

**Yanılgı etiketi:** `pay-sinirini-yanlis-cikarma`

---
### B-21 · FL-4.2.2 · K3
**Senin cevabın:** b (7, 11) · **Doğru cevap:** d (1, 4, 7, 11, 14)

**Neyi soruyor:** %100 2-değerli sınır değer kapsamı zaten sağlanmışken, %100 3-değerli sınır değer kapsamına geçmek için EK olarak hangi parola uzunluklarının test edilmesi gerektiği.

**Doğru şık neden doğru:**
Adım adım türetme:
1. Paylar (değişken: parola uzunluğu, alanın alt sınırı 0 — form boşken uzunluk 0):
   - P1 (geçersiz, çok kısa): 0–5
   - P2 (geçerli): 6–12
   - P3 (geçersiz, çok uzun): 13 ve üzeri
2. Sınır değerler (her payın min ve max'ı): **0, 5, 6, 12, 13** (P3'ün üst sınırı tanımsız/soruda kullanılmıyor).
3. 2-değerli SDA kapsam öğeleri = bu sınır değerlerin kendisi → 0, 5, 6, 12, 13. Soruya göre bunlar ZATEN test edilmiş durumda.
4. 3-değerli SDA kapsam öğeleri = her sınır değer + o sınır değerin iki komşusu:
   - 0 → (-1), 0, **1**  → -1 geçerli bir uzunluk değil, atılır
   - 5 → **4**, 5, 6
   - 6 → 5, 6, **7**
   - 12 → **11**, 12, 13
   - 13 → 12, 13, **14**
5. Birleşim: {1, 4, 5, 6, 7, 11, 12, 13, 14}. Zaten denenmiş olanları (0, 5, 6, 12, 13) çıkar → EK olarak gereken: **1, 4, 7, 11, 14** = d şıkkı.

> ALINTI: "3 değerli SDA'da (Koomen 2006, O'Regan 2019) her sınır değer için üç kapsam öğesi vardır. Bunlar:"
> ALINTI: "sınır değer ve bu sınır değerin her iki komşu sınır değeri. Dolayısıyla 3 değerli SDA'da bazı kapsam"
> ALINTI: "öğeleri sınır değerler olmayabilir. 3 değerli SDA ile %100 kapsama ulaşmak için test senaryolarının tüm"

**Senin şıkkın neden yanlış:** b şıkkı (7, 11) yalnızca GEÇERLİ payın (6–12) içine düşen komşuları ekler; yani sadece "sınırın iç tarafındaki" komşular düşünülmüş. 3-değerli SDA her sınır değerin İKİ komşusunu da ister: dıştaki komşular 4 (5'in altı) ve 14 (13'ün üstü) de kapsam öğesidir. Ayrıca form boşken uzunluk 0 bir sınır değer olduğundan onun komşusu 1 de gereklidir — bu adım tümüyle atlanmış.

**Ayırt edici fark:** 3-değerli SDA her sınır değerin hem alt hem üst komşusunu (4, 7, 11, 14) ve alan alt sınırı 0'ın komşusu 1'i ister; b şıkkı yalnızca geçerli payın iç komşularını sayar.

**Yanılgı etiketi:** `3-degerli-sda-eksik-komsu`

---
### C-20 · FL-4.2.1 · K3
**Senin cevabın:** d (123, 1222, 12345) · **Doğru cevap:** a (12, 1111, 1234, 12345)

**Neyi soruyor:** İki pay grubu (PIN uzunluğu; farklı rakam sayısı) ve her grupta 2 pay olmak üzere toplam 4 payı en iyi kapsayan test verisi grubu.

**Doğru şık neden doğru:**
Adım adım türetme:
1. Pay grubu 1 — PIN uzunluğu: P1a "uzunluk doğru" (tam 4 hane), P1b "uzunluk yanlış" (4'ten farklı).
2. Pay grubu 2 — farklı rakam sayısı: P2a "doğru" (en az iki farklı rakam), P2b "yanlış" (tüm rakamlar aynı).
3. Toplam kapsam öğesi = 4 pay. %100 için hepsi en az bir kez denenmeli.
4. a şıkkının eşlemesi:
   - 12 → uzunluk 2 = P1b; rakamlar {1,2} = P2a
   - 1111 → uzunluk 4 = P1a; tüm rakamlar aynı = P2b
   - 1234 → uzunluk 4 = P1a; farklı rakamlar = P2a
   - 12345 → uzunluk 5 = P1b; farklı rakamlar = P2a
   Kapsanan: P1a ✔, P1b ✔, P2a ✔, P2b ✔ → **4/4 = %100**, üstelik her geçersiz pay tek başına (diğer geçersiz payla birleşmeden) denenmiştir.
5. d şıkkının eşlemesi:
   - 123 → P1b + P2a
   - 1222 → P1a + P2a (1 ve 2 → en az iki farklı rakam)
   - 12345 → P1b + P2a
   Kapsanan: P1a ✔, P1b ✔, P2a ✔, **P2b ✘** → 3/4 = %75.

> ALINTI: "DPA'da kapsam öğeleri denklik paylarıdır. Bu teknikle kapsamın %100'üne ulaşmak için test senaryoları,"
> ALINTI: "her payı en az bir kez kapsama alarak, belirlenmiş tüm payları (geçersiz paylar dahil) denemesi"

(b şıkkı da 4 payı sayısal olarak kapsar gibi görünür; ancak oradaki "1" değeri hem "uzunluk yanlış" hem "tüm rakamlar aynı" paylarını AYNI testte tetikler; iki geçersiz koşulun tek testte birleşmesi kusur maskelenmesi riski taşır. Syllabus bu ilkeyi durum geçişi bağlamında şöyle ifade eder:
> ALINTI: "denemeye çalışmalıdır. Tek bir test senaryosunda yalnızca bir geçersiz geçişin test edilmesi, kusur"
Bunun DPA'ya birebir uygulanışı için doğrudan bir cümle yoktur:
> KAYNAK YOK: syllabus'ta doğrudan karşılık bulunamadı)

**Senin şıkkın neden yanlış:** d şıkkında "1222" değerini muhtemelen "tüm rakamları aynı" payına saydın — oysa 1222 iki farklı rakam (1 ve 2) içerir, dolayısıyla "doğru farklı rakam sayısı" payındadır. Bu yüzden d şıkkında "tüm rakamları aynı" payı hiç test edilmez ve kapsam %75'te kalır. Ayrıca d yalnızca 3 test verisi içerir; 4 payı 3 testle kapsamak ancak her testin iki farklı gruptan pay taşımasıyla mümkündür ve burada bu sağlanmamıştır.

**Ayırt edici fark:** "Tüm rakamlar aynı" payına ancak 1111 gibi tek çeşit rakamdan oluşan bir PIN düşer; 1222 bu paya değil, "en az iki farklı rakam" payına düşer — d bu payı hiç kapsamaz.

**Yanılgı etiketi:** `pay-esleme-hatasi-eksik-pay`

---
### C-21 · FL-4.2.2 · K3
**Senin cevabın:** b (99, 100, 200, 201) · **Doğru cevap:** d (101, 150, 199, 200)

**Neyi soruyor:** `EĞER (değer ≤ 100 VEYA değer ≥ 200) İSE "değer yanlış"` kuralı için 2-değerli SDA açısından en geniş kapsamı sağlayan girdi grubu.

**Doğru şık neden doğru:**
Adım adım türetme:
1. Koşulu çöz: "değer TAMAM" ancak `değer > 100 VE değer < 200` iken yazılır → **geçerli pay = 101…199**.
2. Paylar: P1 = (…, 100] geçersiz; P2 = [101, 199] geçerli; P3 = [200, …) geçersiz.
3. Sınır değerler (her payın min/max'ı, alan uçları hariç): **100, 101, 199, 200** → 4 kapsam öğesi.
4. Şıkların kapsamı:
   - a) 100 ✔, 150 ✘(sınır değil), 200 ✔, 201 ✘ → 2/4 = %50
   - b) 99 ✘, 100 ✔, 200 ✔, 201 ✘ → 2/4 = %50
   - c) 98 ✘, 99 ✘, 100 ✔, 101 ✔ → 2/4 = %50
   - d) **101 ✔, 150 ✘, 199 ✔, 200 ✔ → 3/4 = %75**
5. En geniş kapsam d şıkkında.

> ALINTI: "SDA sadece sıralı verilerden oluşan paylarda kullanılabilir. Bir payın minimum ve maksimum değerleri o"
> ALINTI: "değer ve bitişik paya ait en yakın komşusu. 2 değerli SDA ile %100 kapsama ulaşmak için test"
> ALINTI: "senaryolarının tüm kapsam öğelerini, yani tanımlanan tüm sınır değerlerini denemesi gerekir."

**Senin şıkkın neden yanlış:** b şıkkı (99, 100, 200, 201) sınırları 99/100 ve 200/201 çiftleri olarak alır. Bu, geçerli aralığın 100–200 olduğu varsayımından çıkar — yani `≤ 100` ve `≥ 200` operatörlerinin kapsayıcı (dahil) olduğunun gözden kaçırılmasından. 100 ve 200 aslında GEÇERSİZ paya aittir; geçerli payın uçları 101 ve 199'dur. 99 ve 201 ise hiçbir payın min/max'ı değildir (P1'in içi ve P3'ün içi), dolayısıyla sınır değer sayılmaz ve kapsama katkı vermez.

**Ayırt edici fark:** `≤ 100` ve `≥ 200` dahil olduğu için geçerli pay 101–199'dur; sınır değerler 100/101 ve 199/200'dür — 99 ve 201 sınır değer değildir.

**Yanılgı etiketi:** `karsilastirma-operatoru-siniri-kaydirma`

---
### C-22 · FL-4.2.3 · K3
**Senin cevabın:** c · **Doğru cevap:** d (C1 = Y, C2 = Y, C3 = Y)

**UYARI:** tablo yapısı metin çıkarımında kısmen kaybolmuş, analiz sınırlı. Koşul sütunları kurtarılabildi (R1: C1=–, C2=D, C3=D | R2: C1=–, C2=Y, C3=– | R3: C1=Y, C2=–, C3=Y), fakat hangi "X" hangi aksiyon satırına denk geliyor okunamıyor. Aşağıdaki türetme yalnızca KOŞUL sütunlarına dayanır; aksiyon eşlemesi varsayım olarak "her kural farklı bir aksiyon tetikler" alınmıştır (tabloda üç kural ve üç aksiyon var, her kuralda tek X işaretli).

**Neyi soruyor:** Karar tablosunda ÇELİŞKİLİ kural bulunduğunu ortaya koyan girdi kombinasyonu — yani aynı girdide birden fazla kuralın eşleşip farklı aksiyonlar dayattığı durum.

**Doğru şık neden doğru:**
Adım adım türetme (D = koşul doğru, Y = koşul yanlış, – = ilgisiz, her değere uyar):
1. d) C1=Y, C2=Y, C3=Y girdisini her kurala karşı sına:
   - R1 (–, D, D): C2 = Y ≠ D → eşleşmez.
   - R2 (–, Y, –): C2 = Y ✔, diğerleri ilgisiz ✔ → **eşleşir**.
   - R3 (Y, –, Y): C1 = Y ✔, C3 = Y ✔ → **eşleşir**.
2. Tek bir girdi hem R2'ye hem R3'e uyuyor ve bu iki kural farklı aksiyonlar dayatıyor → **çelişki**. Doğru cevap d.
3. Karşılaştırma için diğer şıklar:
   - a) (D, D, Y): R1 C3'te düşer, R2 C2'de düşer, R3 C1'de düşer → hiçbir kural eşleşmez. Bu ÇELİŞKİ değil, tablodaki bir BOŞLUKTUR (eksiklik).
   - b) (D, Y, D): yalnızca R2 eşleşir (R3, C1 = D olduğu için düşer) → tek kural, çelişki yok.
   - c) (D, D, D) ve (Y, D, D): her ikisinde de yalnızca R1 eşleşir (R2 C2'de, R3 C3'te düşer) → çelişki yok.

> ALINTI: "Bunlar tablonun satırlarını oluşturur. Her sütun, koşulların benzersiz bir kombinasyonunu ve ilişkili"
> ALINTI: "aksiyonları tanımlayan bir karar kuralına karşılık gelir."
> ALINTI: ""–", koşulun değerinin aksiyon çıktısı açısından ilgisiz olduğu anlamına gelir."
> ALINTI: "yönelik sistematik bir yaklaşım sağlamasıdır. Ayrıca gereksinimlerdeki boşlukları veya çelişkileri bulmaya da"

**Senin şıkkın neden yanlış:** c şıkkında verilen iki girdi (D,D,D) ve (Y,D,D) yalnızca R1 ile eşleşir; C1 değeri R1'de "–" (ilgisiz) olduğu için ikisi de aynı tek kuralı ve aynı aksiyonu üretir. Bu bir çelişki değil, "–" işaretinin beklenen davranışıdır. Muhtemel hatalı adım: "–" sembolünü, aynı satırda iki farklı sonuç doğuran bir belirsizlik olarak okumak; oysa "–" o koşulun çıktıyı etkilemediğini söyler ve tek bir kural altında birleştirilmiş sütunları gösterir.

**Ayırt edici fark:** Çelişki, TEK bir girdinin BİRDEN FAZLA kurala uyup FARKLI aksiyonlar tetiklemesidir (d: R2 ve R3 birlikte tetiklenir); c'deki iki girdi ise aynı tek kurala (R1) düşer.

**Yanılgı etiketi:** `karar-tablosu-ilgisiz-koşul-yorumu`

---
### C-23 · FL-4.2.4 · K3
**Senin cevabın:** d (6) · **Doğru cevap:** a (3)

**UYARI:** durum geçiş diyagramı bir görsel olduğu için metin çıkarımında tamamen kaybolmuş (`raw/SinavC.txt` satır 1002'de yalnızca soru cümlesi var, diyagram yok); bu spesifik diyagramdan sayı TÜRETİLEMEZ. Aşağıda teknik genel olarak açıklanmakta ve şıkların mantığı yorumlanmaktadır.

**Neyi soruyor:** Verilen durum geçiş diyagramında %100 geçerli geçiş kapsamı (0-anahtar kapsamı) için gereken EN AZ test senaryosu sayısı.

**Doğru şık neden doğru:** %100 geçerli geçiş kapsamının doğru yöntemi:
1. Diyagramdaki TÜM geçerli geçişleri listele — bunlar kapsam öğeleridir.
2. Başlangıç durumundan başlayıp mümkün olduğunca çok geçişi ARDIŞIK olarak zincirleyen yollar kur; bir test senaryosu bir olay dizisidir ve tek bir test birçok geçişi peş peşe kapsayabilir.
3. Gereken test senaryosu sayısı = tüm geçişleri örtmek için gereken MİNİMUM yol sayısıdır; bu sayı neredeyse her zaman geçiş sayısından çok daha küçüktür.
4. Bu soruda resmî cevap 3'tür; yani diyagramdaki geçerli geçişler 3 yol ile tümüyle örtülebilmektedir.

> ALINTI: "Geçerli geçişler kapsamında (0-anahtar kapsamı da denir) kapsam öğeleri tekil geçerli geçişlerdir."
> ALINTI: "Geçerli geçişler kapsamının %100'üne ulaşmak için test senaryoları tüm geçerli geçişleri denemelidir."
> ALINTI: "değişikliğiyle (ve gerekirse aksiyonla) sonuçlanan bir dizi olayla temsil edilir. Bir test senaryosu,"
> ALINTI: "durumlar arası çeşitli geçişleri içerebilir."

**Senin şıkkın neden yanlış:** 6 seçeneği, büyük olasılıkla diyagramdaki GEÇİŞ sayısını (veya durum sayısını) doğrudan test senaryosu sayısı olarak yazmaktan çıkar — yani "her geçiş için bir test" varsayımı. Bu yanlış adımdır: bir test senaryosu bir olay DİZİSİdir ve tek bir yol boyunca birden çok geçişi kapsar; bu yüzden minimum test sayısı geçiş sayısından küçüktür.

**Ayırt edici fark:** Kapsam öğesi sayısı (geçerli geçiş sayısı) ile test senaryosu sayısı aynı şey değildir; bir test senaryosu bir yol boyunca birden çok geçişi kapsadığı için minimum test sayısı geçiş sayısından daha azdır.

**Yanılgı etiketi:** `kapsam-ogesi-sayisini-test-sayisi-sanma`

---
### D-19 · FL-4.1.1 · K2
**Senin cevabın:** a (Beyaz kutu test teknikleri) · **Doğru cevap:** b (Kara kutu test teknikleri)

**Neyi soruyor:** Bir GEREKSİNİME (REQ 05-017) dayalı sistem testi senaryoları tasarlarken hangi teknik kategorisinin en faydalı olduğu.

**Doğru şık neden doğru:** Gereksinim bir davranış spesifikasyonudur ("tutar 100 $'ı aşarsa %5 indirim, aksi hâlde indirim yok"). Bu ifade doğrudan denklik payları (≤100 $ / >100 $) ve sınır değerler (100, 100,01 gibi) üretir. Kara kutu (spesifikasyon bazlı) teknikler tam olarak bunun için, yani iç yapıya bakmadan davranışı analiz etmek için kullanılır; ayrıca sistem testi seviyesinde ve gereksinim tabanlı çalışırken en uygun kategoridir.

> ALINTI: "Kara kutu test teknikleri (spesifikasyon bazlı teknikler olarak da bilinir) test nesnesinin iç yapısına atıfta"
> ALINTI: "bulunulmadan test nesnesinin davranışının analiz edilmesine dayanır. Bu nedenle test senaryoları"
> ALINTI: "yazılımın nasıl yazıldığından bağımsızdır. Sonuç olarak, kod değişir ancak test nesnesinin davranışı aynı"

**Senin şıkkın neden yanlış:** Beyaz kutu (yapı bazlı) teknikler test nesnesinin İÇ YAPISININ analizine dayanır ve ancak kodun tasarımı/kodlanması sonrasında test senaryosu üretebilir. Soruda elimizde kod değil, bir gereksinim cümlesi var — kaynak kod veya kontrol akış grafiği verilmemiştir. Muhtemelen "%5 indirim / aksi takdirde" ifadesindeki if-else yapısı görülüp bu bir "karar/dal" testi zannedildi; ancak bu koşul spesifikasyonda tanımlanmış bir İŞ KURALIdır, koddaki bir karar ifadesi değildir. (c riskli değil ama gereksinim varken sistematik teknik yerine tecrübeye dayalıdır; d ise bir teknik kategorisi değil, test yaklaşımıdır.)

**Ayırt edici fark:** Girdi kaynağı gereksinim/spesifikasyon ise kara kutu, kaynak kod/iç yapı ise beyaz kutu teknikleri kullanılır; burada elde yalnızca gereksinim vardır.

**Yanılgı etiketi:** `spesifikasyondaki-kosulu-kod-karari-sanma`

---

## Tekrar Eden Yanılgı Özeti

| Etiket | Sorular | Kısa tanım |
|---|---|---|
| `each-choice-yerine-kombinasyon-sayma` | A-20 | Her payı kapsamak yerine pay kombinasyonları sayılıyor |
| `sda-kapsamini-dpa-kapsami-sanma` | A-21 | SDA kapsam öğesi sınır değerken pay sayılıyor |
| `karar-tablosunu-beyaz-kutu-sanma` | B-19 | Karar tablosunun kaynağı spesifikasyon değil kod sanılıyor |
| `spesifikasyondaki-kosulu-kod-karari-sanma` | D-19 | Gereksinimdeki if-else iş kuralı, koddaki karar ifadesi sanılıyor |
| `pay-sinirini-yanlis-cikarma` | B-20 | Payı belirleyen davranış kuralı yanlış uygulanıyor |
| `pay-esleme-hatasi-eksik-pay` | C-20 | Bir test verisi yanlış paya atanınca bir pay hiç kapsanmıyor |
| `3-degerli-sda-eksik-komsu` | B-21 | 3-değerli SDA'da dış komşular ve alan uç sınırı atlanıyor |
| `karsilastirma-operatoru-siniri-kaydirma` | C-21 | ≤ / ≥ dahil olduğu gözden kaçıp sınır bir birim kayıyor |
| `karar-tablosu-ilgisiz-koşul-yorumu` | C-22 | "–" (ilgisiz) sembolü çelişki gibi okunuyor |
| `kapsam-ogesi-sayisini-test-sayisi-sanma` | C-23 | Geçiş sayısı doğrudan test senaryosu sayısı sanılıyor |

**Örüntü 1 — Kaynak karışıklığı (kara kutu / beyaz kutu ayrımı):** B-19 ve D-19'da aynı kök hata var; spesifikasyondaki koşullar koddaki karar yapılarıyla karıştırılıyor. Kural: *Girdi kaynağı gereksinim ise kara kutu, kod ise beyaz kutu.*

**Örüntü 2 — "Kapsam öğesi nedir?" sorusunun atlanması:** A-21, C-23 ve kısmen A-20'de kapsam yüzdesi/test sayısı hesaplanırken önce kapsam öğesinin ne olduğu (pay mı, sınır değer mi, geçiş mi, sütun mu) belirlenmiyor. Her K3 sorusunda ilk adım bu olmalı: *kapsam öğesini adlandır → toplam sayısını bul → kaç tanesinin dendiğini say → böl.*

**Örüntü 3 — Sınır tespitinde bir birim kayma / eksik komşu:** B-21 ve C-21. Kural: *Önce geçerli payın tam uçlarını (dahil/hariç dikkate alarak) yaz, sonra 2-değerli için uçları + karşı komşuları, 3-değerli için her sınır değerin İKİ komşusunu da ekle.*

## Bölüm 4 — Beyaz Kutu, Tecrübeye Dayalı ve İşbirlikçi Teknikler  (8 soru)

### A-27 · FL-4.4.2 · K2
**Senin cevabın:** b · **Doğru cevap:** c

**Neyi soruyor:** Gereksinim listesi henüz elinizde yokken, zaman baskısı altında, alan bilgisi ve analitik beceriye sahip bir test uzmanının hızlıca test sonucu üretmesi gereken durumda hangi tecrübeye dayalı tekniğin EN UYGUN olduğu soruluyor. Soru, tekniklerin "uygulanma koşullarını" ayırt etmenizi istiyor.

**Doğru şık neden doğru:** Sorudaki üç sinyalin üçü de doğrudan keşif testinin ders programındaki tanım ve uygulanabilirlik koşullarına karşılık geliyor: (1) gereksinimler henüz paylaşılmamış = "gereksinimler az veya yetersiz", (2) canlıya alma gecikmesi + geç başlayan koşum = "zaman baskısı", (3) alan bilgisi + iyi analiz becerisi = keşif testinin etkinliğini artıran test uzmanı profili.

> ALINTI: "Keşif testleri, gereksinimler az veya yetersiz olduğunda veya testler üzerinde önemli bir zaman baskısı"

> ALINTI: "uzmanı deneyimli, alan bilgisine sahip ve analitik beceriler, merak ve yaratıcılık gibi üst seviye temel"

Ayrıca keşif testi, önceden hazır bir spesifikasyona veya hazır test senaryolarına ihtiyaç duymaz; tasarım ve koşum eş zamanlı yürür, bu da "hemen sonuç üret" baskısına birebir uyar:

> ALINTI: "Keşif testinde, test uzmanı test nesnesi hakkında bilgi edinirken testler eş zamanlı olarak tasarlanır,"

**Senin şıkkın neden yanlış:** b) Hata tahmini de tecrübeye dayalı bir tekniktir, ancak ders programında tanımı "geçmiş davranış / geliştiricilerin yaptığı kusurlar / benzer uygulamalardaki arızalar" bilgisine dayanan, **belirli hata hipotezlerini hedefleyen** bir tekniktir. Sorudaki tetikleyiciler (gereksinim yokluğu + zaman baskısı + öğrenerek ilerleme) hata tahmininin tanımına değil, keşif testinin uygulanabilirlik koşullarına aittir. Hata tahmini "nerede hata olabilir" sorusunu cevaplar; soru ise "ürünü hiç tanımadan nasıl kapsamlı sonuç üretirim" durumunu tarif ediyor.

> ALINTI: "Hata tahminleme, test uzmanının bilgilerine dayalı olarak insan hatalarının, yazılım hatalarının ve"

**Ayırt edici fark:** Keşif testi bilinmeyen bir test nesnesini öğrenirken eş zamanlı test tasarlar (gereksinim yoksa/zaman darsa); hata tahmini ise zaten sahip olunan hata bilgisiyle spesifik arıza hipotezlerini hedefler.

**Yanılgı etiketi:** `hata-tahmini-kesif-testi-karisikligi`

---
### B-27 · FL-4.4.3 · K2
**Senin cevabın:** b · **Doğru cevap:** d

**Neyi soruyor:** Verilen dört ifadeden hangisinin gerçek bir **kontrol listesi öğesi** olabileceğini soruyor. Yani "kontrol listesi öğesi olma kriterleri" ile "kontrol listesine giremeyecek öğeler" ayrımını test ediyor.

**Doğru şık neden doğru:** d) "Hata mesajları kullanıcının anlayabileceği bir dilde yazılmıştır" — bu, tek tek ve doğrudan kontrol edilebilir (bir ekranı açıp hata mesajına bakarsınız), bir kalite karakteristiğine (kullanılabilirlik) ilişkin bir test koşuludur ve otomatik olarak kontrol edilemeyecek, insan yargısı gerektiren türdendir. Ders programının kontrol listesi öğesi tanımına birebir oturur:

> ALINTI: "Kontrol listesi öğeleri genellikle soru şeklindedir. Her öğe ayrı ayrı ve doğrudan kontrol edilebilir olmalıdır."

> ALINTI: "Bu öğeler gereksinimlere, arayüz özelliklerine, kalite karakteristiğine veya diğer test koşulu biçimlerine"

Kontrol listelerinin neyi **içermemesi** gerektiği de açıkça yazılıdır — bu kural, diğer üç şıkkı eleyen filtredir:

> ALINTI: "otomatik olarak kontrol edilebilecek öğeleri, daha çok giriş/çıkış kriteri olmaya uygun olan öğeleri veya"

> ALINTI: "çok genel olan öğeleri içermez (Brykczynski 1999)."

**Senin şıkkın neden yanlış:** b) "Elde edilen komut kapsamı %85'i aşıyor" — bu, ölçülebilir bir eşik ifadesidir; klasik bir **çıkış kriteri** (test tamamlama kriteri) ve aynı zamanda bir araçla **otomatik olarak kontrol edilebilen** bir ölçüdür. Ders programı bu iki niteliği taşıyan öğeleri kontrol listesi dışında bırakır. Muhtemelen "kontrol edilebilir olmalı" kuralını "ölçülebilir olmalı" diye okuyup, ölçülebilirliği tek başına yeterli sandınız; oysa asıl ayraç öğenin bir *test koşulu* mu yoksa bir *giriş/çıkış kriteri* mi olduğudur.

Diğer çeldiriciler de aynı filtreyle eleniyor: a) bir insan hatası (error) ifadesidir, kontrol edilecek bir koşul değil; c) "program fonksiyonel ve fonksiyonel olmayan gereksinimler açısından doğru çalışıyor" ise "çok genel" olduğu için dışlanır.

**Ayırt edici fark:** Kontrol listesi öğesi, tek tek ve doğrudan kontrol edilebilen bir **test koşuludur**; kapsam yüzdesi eşiği ise otomatik ölçülebilen bir **çıkış kriteridir** ve kontrol listesine girmez.

**Yanılgı etiketi:** `kontrol-listesi-ogesi-vs-cikis-kriteri`

---
### C-24 · FL-4.3.2 · K2
**Senin cevabın:** b · **Doğru cevap:** c

**UYARI:** tablo/kod yapısı metin çıkarımında kaybolmuş, analiz sınırlı. Soru bir **kontrol akış grafiği görseline** dayanıyor; grafik pakete metin olarak aktarılamamış. Bu nedenle "8" sayısını grafikten türetemem ve türetmeye çalışmam da uydurma olur. Aşağıda tekniğin doğru sayma yöntemini adım adım veriyorum; bunu sınav kitapçığındaki grafiğe kendin uygula.

**Neyi soruyor:** Dal testi uygulanacaksa **kaç kapsam öğesi** test edilmesi gerektiğini soruyor. Yani "dal testinde kapsam öğesi nedir?" sorusunun sayısal karşılığı.

**Doğru şık neden doğru:** Dal testinde kapsam öğesi = **dal**, yani kontrol akış grafiğinde iki düğüm arasındaki her bir kontrol transferi (grafikteki her bir ok/kenar). Kritik nokta: sadece koşullu dallar değil, **koşulsuz dallar da** sayılır.

> ALINTI: "Dal testlerinde kapsam öğeleri dallardır ve burada amaç, kabul edilebilir bir kapsama seviyesi elde"

> ALINTI: "veya koşullu (ör. karar çıktısı) olabilir."

> ALINTI: "%100 dal kapsamına ulaşıldığında, kod içindeki koşulsuz ve koşullu tüm dallar test senaryoları tarafından"

Doğru sayma adımları (bu grafiğe uygulanacak yöntem):
1. Grafikteki **düğümleri** değil, **okları (kenarları)** say — dal testinde kapsam öğesi düğüm değil, kontrol transferidir.
2. Her karar düğümünden çıkan okların hepsini ayrı ayrı say (bir `if` düğümünden 2 ok: true ve false; bir `switch/case` düğümünden case sayısı kadar ok; bir döngü düğümünden 2 ok: döngüye devam ve döngüden çıkış).
3. Karar olmayan, düz akış (koşulsuz) oklarını da listeye **ekle** — en sık atlanan adım budur.
4. Toplam ok sayısı = test edilmesi gereken kapsam öğesi sayısı. Kapsam yüzdesi ise şu formülle hesaplanır:

> ALINTI: "tarafından denenen dal sayısının toplam dal sayısına bölünmesiyle ölçülür ve yüzde olarak ifade edilir."

Yani %100 dal kapsamı için: (denenen dal sayısı / toplam dal sayısı) = N/N. Resmî cevap 8 olduğuna göre grafikte toplam 8 kenar bulunmaktadır.

**Senin şıkkın neden yanlış:** b) 4 — bu değer, tipik olarak **yalnızca koşullu dalları** saymaktan çıkar: grafikte 2 karar düğümü varsa 2 × 2 = 4 karar çıktısı sayılır ve aradaki koşulsuz kontrol transferleri (düz akış okları, birleşme sonrası oklar, giriş/çıkış okları) hesaba katılmaz. Aynı sayı, "kapsam öğesi = karar" veya "kapsam öğesi = düğüm/komut bloğu" varsayımından da çıkabilir. Her üç yol da aynı temel hataya dayanır: dal testinin kapsam öğesini karar/komut sanmak.

> ALINTI: "Komut testinde kapsam öğeleri çalıştırılabilir komutlardır."

**Ayırt edici fark:** Dal testinin kapsam öğesi grafikteki **her kontrol transferi (koşullu + koşulsuz kenar)** iken, senin saydığın büyüklük yalnızca karar çıktıları / düğümlerdir; koşulsuz dallar sayıma dahil edilmediği için sonuç eksik çıkar.

**Yanılgı etiketi:** `ifade-dal-kapsami-karisikligi`

---
### C-25 · FL-4.3.3 · K2
**Senin cevabın:** b · **Doğru cevap:** a

**Neyi soruyor:** Beyaz kutu testinin, kara kutu testine sağladığı katkının ders programında yazılı olan gerekçesini soruyor (FL-4.3.3 "Beyaz Kutu Testinin Önemi").

**Doğru şık neden doğru:** a) Ders programı, sadece kara kutu testi yapmanın gerçek kod kapsamını ölçmediğini ve beyaz kutu kapsam ölçülerinin objektif bir ölçüm sağladığını açıkça söyler. Yani kara kutu testleri koşulduktan sonra elde edilen kod kapsamına bakarak, o kara kutu test setinin ne kadar yeterli olduğu **değerlendirilebilir** ve boşlukları kapatacak ek testler üretilebilir.

> ALINTI: "Sadece kara kutu testi gerçekleştirmek, gerçek kod kapsamının ölçülmesini sağlamaz."

> ALINTI: "kapsam ölçüleri objektif bir kapsam ölçümü sağlar ve bu kapsamı büyütmek için üretilecek ek testlere"

**Senin şıkkın neden yanlış:** b) "Ulaşılamayan (erişilemez) kaynak kodu parçalarını belirleme" — bu, kapsam analizinin pratikte yan ürünü olabilecek doğru bir gözlem gibi görünür, ancak (i) ders programında böyle bir ifade yer almaz ve (ii) daha önemlisi soru "beyaz kutu, **kara kutu testini desteklemeye** nasıl yardım eder" diye soruyor. Erişilemez kod tespiti kara kutu testine bir katkı değil, kodun kendisine dair ayrı bir bulgudur. Şıkkı seçerken sorunun "kara kutuyu destekleme" kısıtını gözden kaçırıp genel olarak "beyaz kutunun faydası" listesinden makul görüneni işaretlemişsin.

> KAYNAK YOK: syllabus'ta "ulaşılamayan/erişilemez kod parçalarının belirlenmesi" ifadesine doğrudan karşılık bulunamadı

Diğer çeldiriciler: c) yanlıştır çünkü dal kapsamı yalnızca komut kapsamını içerir, kara kutu tekniklerini değil — "> ALINTI: "Dal kapsamı, komut kapsama yüzdesini içerir."" Kara kutu tekniklerinin kapsam öğeleri (denklik payları, sınır değerler, karar tablosu kuralları, durum geçişleri) tamamen farklıdır ve %100 dal kapsamı bunları garanti etmez. d) ise ilişkiyi ters çevirir: kara kutu tekniklerinin kapsam öğelerini beyaz kutu değil, kara kutu tekniklerinin kendisi üretir.

**Ayırt edici fark:** Doğru şık, beyaz kutu kapsam ölçülerini kara kutu test setinin **yeterliliğini objektif olarak değerlendiren bir ölçüm aracı** olarak konumlandırır; senin şıkkın ise kapsam analizini kara kutuyla ilgisi olmayan bir kod bulgusu (erişilemez kod) üretimine bağlar.

**Yanılgı etiketi:** `beyaz-kutu-kapsam-olcusunun-amaci`

---
### C-26 · FL-4.4.1 · K2
**Senin cevabın:** a · **Doğru cevap:** b

**Neyi soruyor:** "Doğru girdi kabul edilmedi / Yanlış girdi kabul edildi / Yanlış çıktı biçimi / Sıfıra bölme" şeklinde önceden hazırlanmış bir **olası hata listesini** kullanan test uzmanının hangi tekniği uyguladığını soruyor.

**Doğru şık neden doğru:** b) Kusur ortaya çıkarmaya yönelik saldırı (fault attack), hata tahminlemenin metodik uygulanma biçimidir ve tam olarak "olası insan hataları, yazılım hataları ve arızalardan oluşan bir liste oluşturup/edinip bunları hedefleyen testler tasarlamak" demektir. Sorudaki liste birebir bu tanımdır.

> ALINTI: "Kusur ortaya çıkarmaya yönelik saldırılar hata tahminlemenin uygulanmasına yönelik metodik bir"

> ALINTI: "listesini oluşturması veya elde etmesi ve insan hatalarıyla ilişkili hataları tanımlayacak, hataları ortaya"

Listedeki dört maddenin her biri, ders programının hata kategorileri örnekleriyle kelimesi kelimesine örtüşür — bu, listenin bir "hata listesi" olduğunun kanıtıdır: "doğru girdi kabul edilmedi" = girdi, "yanlış çıktı biçimi" = çıktı (yanlış format), "sıfıra bölme" = hesaplama.

> ALINTI: "Genel olarak insan hataları, yazılım hataları ve arızalar şunlarla ilgili olabilir: girdi (ör. doğru girdinin kabul"

> ALINTI: "edilmemesi, yanlış veya eksik parametreler), çıktı (ör. yanlış format, yanlış sonuç), mantık (ör. eksik"

**Senin şıkkın neden yanlış:** a) Keşif testi — keşif testinde önceden hazırlanmış bir madde listesi kullanılmaz; testler test nesnesi öğrenilirken eş zamanlı tasarlanır ve kapsam öğeleri önceden değil, oturum sırasında belirlenir. Elinizde önceden yazılmış dört maddelik bir liste varsa tanım gereği keşif testi yapmıyorsunuzdur.

> ALINTI: "test oturumunda tanımlanır ve denenir."

**Not (en yakın çeldirici):** c) Kontrol listesine dayalı test de "liste" kullanır ve bu yüzden cazip görünür. Fark şudur: kontrol listesi öğeleri **test koşullarıdır** (genellikle soru formunda, "… doğru çalışıyor mu?"), kusur saldırısı listesi ise **arıza/hata tipleridir** ("… hatalı oldu"). Sorudaki dört madde bir koşul değil, birer arıza tarifidir. d) Sınır değer analizi ise bir kara kutu tekniğidir, hata listesiyle ilgisi yoktur.

**Ayırt edici fark:** Kusur saldırısında liste **olası hata/arızalardan** oluşur ve hata tahmininin metodik biçimidir; keşif testinde ise önceden liste yoktur, kapsam öğeleri test oturumu sırasında belirlenir.

**Yanılgı etiketi:** `hata-tahmini-kesif-testi-karisikligi`

---
### C-27 · FL-4.4.3 · K2
**Senin cevabın:** a · **Doğru cevap:** d

**Neyi soruyor:** Kontrol listesine dayalı testin neden **daha geniş kapsam** üretebildiğinin ders programındaki gerekçesini soruyor. Buradaki anahtar, kapsam artışının hangi mekanizmadan doğduğu.

**Doğru şık neden doğru:** d) Ders programı kapsam genişlemesini doğrudan kontrol listelerinin **üst seviye** olmasına ve bu yüzden gerçek koşumda test uzmanından test uzmanına değişiklik göstermesine bağlar. Aynı üst seviye maddeden yola çıkan iki test uzmanı farklı testler tasarlar; bu çeşitlilik kapsamı büyütür, bedeli ise tekrarlanabilirliğin düşmesidir.

> ALINTI: "Bu kontrol listeleri üst seviye listeler olduğu için, gerçek testlerde bazı değişikliklerin ortaya çıkması"

> ALINTI: "muhtemeldir; bu da potansiyel olarak daha büyük kapsama ama daha düşük tekrarlanabilirliğe yol açar."

**Senin şıkkın neden yanlış:** a) "Kontrol listesi öğeleri yeterince **düşük** bir ayrıntı düzeyinde tanımlanabilir…" — bu, ders programının söylediğinin tam tersidir. Kapsam artışını sağlayan şey maddelerin ayrıntılı/düşük seviyeli olması değil, **üst seviye** olmasıdır. Ayrıca ders programı, kontrol listelerinin ayrıntılı test senaryolarının yerine geçmediğini, onların bulunmadığı durumlarda yol gösterici olduğunu söyler:

> ALINTI: "Ayrıntılı test senaryolarının olmadığı durumlarda, kontrol listesine dayalı testler, test süreci için yol gösterici"

Muhtemel hatalı akıl yürütmen: "daha ayrıntılı madde → daha ayrıntılı test → daha çok kapsam" sezgisi. Ders programında kapsam, ayrıntıdan değil, üst seviye maddenin yorum serbestliğinden (varyasyondan) doğar.

Diğer çeldiriciler: b) yanlıştır, çünkü kontrol listeleri otomatik kontrol edilebilecek öğeleri zaten içermez — "> ALINTI: "otomatik olarak kontrol edilebilecek öğeleri, daha çok giriş/çıkış kriteri olmaya uygun olan öğeleri veya"". c) ise ders programında yer almayan bir "her öğe ayrı ve bağımsız test edilmelidir → farklı alanları kapsar" kuralı uydurur; ders programı öğelerin ayrı ayrı **kontrol edilebilir** olmasını ister, bu bir kapsam genişletme mekanizması değildir.

**Ayırt edici fark:** Kapsam genişlemesinin kaynağı, maddelerin ayrıntılı olması değil, **üst seviye olmaları nedeniyle koşumda ortaya çıkan varyasyondur** (bedeli: düşük tekrarlanabilirlik).

**Yanılgı etiketi:** `kontrol-listesi-ust-seviye-varyasyon`

---
### C-28 · FL-4.5.2 · K2
**Senin cevabın:** c · **Doğru cevap:** b

**Neyi soruyor:** Kabul kriterlerinin iki yaygın formatından biri olan **senaryo odaklı** (BDD Given/When/Then) formata en iyi örneğin hangisi olduğunu soruyor.

**Doğru şık neden doğru:** b) "Bir müşteri sepetine bir ürün ekleyip ödeme işlemine geçtiğinde, henüz yapmamışsa oturum açması veya bir hesap oluşturması istenmelidir." Bu cümle Given/When/Then iskeletini taşır: **Given** (henüz oturum açmamış bir müşteri) — **When** (sepete ürün ekleyip ödemeye geçtiğinde) — **Then** (oturum açması veya hesap oluşturması istenir). Yani bir bağlam + bir tetikleyici olay + gözlemlenebilir bir sonuç içeren somut bir senaryodur.

> ALINTI: "Senaryo odaklı (ör. BDD'de kullanılan Given/When/Then formatı, bkz. bölüm 2.1.3)"

Kabul kriterinin işlevi de bunu destekler: kabul kriterleri test uzmanının deneyeceği test koşullarıdır ve hem pozitif hem negatif senaryoları açıklar.

> ALINTI: "Bir kullanıcı hikayesi için kabul kriterleri, bu kullanıcı hikayesinin, paydaşlar tarafından kabul edilmesi için"

**Senin şıkkın neden yanlış:** c) `IF (contain(product(23).Name, cart.products())) THEN return FALSE` — bu bir **kod/uygulama parçasıdır**, kabul kriteri değildir. Kabul kriterleri paydaşlar arasında fikir birliği sağlamak için yazılır ve paydaşların anlayabileceği bir dilde ifade edilmelidir; sözde kod bu işlevi görmez. Muhtemelen "IF … THEN" yapısını "When … Then" senaryo yapısıyla eşleştirdin; ancak Given/When/Then bir **doğal dil senaryo şablonudur**, programlama dilindeki koşul ifadesi değildir.

Diğer çeldiriciler: a) ve d) kabul kriteri olarak geçerlidir ama **kural odaklı** formattadır — tetikleyici olay ve bağlam içermeyen, "…meli/…malı" biçiminde genel kurallardır:

> ALINTI: "Kural odaklı (ör. madde işaretli kontrol listesi veya girdi-çıktı eşlemesinin tablo haline getirilmiş şekli)"

**Ayırt edici fark:** Senaryo odaklı kabul kriteri, doğal dilde bağlam–olay–sonuç (Given/When/Then) üçlüsünü kurar; senin seçtiğin şık ise doğal dil senaryosu değil, uygulama düzeyinde bir kod/koşul ifadesidir.

**Yanılgı etiketi:** `senaryo-odakli-vs-kural-odakli-kabul-kriteri`

---
### D-28 · FL-4.5.1 · K2
**Senin cevabın:** b · **Doğru cevap:** d

**Neyi soruyor:** İş birliğine dayalı kullanıcı hikayesi yazımında, ekibin **neyin teslim edilmesi gerektiği konusunda ortak anlayışa** varmasını hangi yöntemin sağladığını soruyor. Anahtar ifade "ortak anlayış / ortak vizyon".

**Doğru şık neden doğru:** d) Konuşmalar (Conversations) — kullanıcı hikayesinin "3 C" unsurlarından biridir ve tanımı gereği yazılımın nasıl kullanılacağını açıklayan iletişim biçimidir. Ders programı, iş birliğinin (analiz–geliştirme–test perspektiflerinin bir araya gelmesinin) neyin teslim edileceğine dair ortak vizyon sağladığını doğrudan söyler.

> ALINTI: "Conversation (Konuşmalar): Yazılımın nasıl kullanılacağını açıklar (belgeyle veya sözlü olabilir)"

> ALINTI: "birliği, ekibin analiz, yazılım geliştirme ve test etme gibi üç perspektifi dikkate alarak, neyin teslim edilmesi"

> ALINTI: "gerektiğine yönelik ortak bir vizyon edinmesini sağlar."

Ayrıca kabul kriterleri de bu konuşmaların sonunda ortaya çıkar; yani ortak anlayışın kaynağı konuşmalardır:

> ALINTI: "Kabul kriterleri genelde bir konuşma"

**Senin şıkkın neden yanlış:** b) Gözden geçirme (reviews) — gözden geçirmeler gerçekten de tutarsızlık ve çelişkileri **tespit eder**, ama bu bir doğrulama/kusur tespiti faaliyetidir (Bölüm 3), sorunun aradığı "neyin teslim edileceğine dair ortak anlayışın **oluşturulması**" değildir. Şıkkın kendi gerekçesi bile ("tutarsızlıkları ve çelişkileri tespit edebilir") ortak anlayış üretmeyi değil, hata bulmayı tarif ediyor — sorunun anahtar ifadesiyle eşleşmiyor. Şık metnindeki gerekçe cümlesini okumak, bu tuzağı doğrudan eler.

> KAYNAK YOK: syllabus'un 4.5.1 bölümünde gözden geçirmelerin kullanıcı hikayesi yazımında ortak anlayış sağladığına dair bir ifade bulunamadı

Diğer çeldiriciler aynı testten geçemez: a) Poker planlama **efor** üzerinde fikir birliği sağlar (kapsam/anlayış değil), c) döngü planlaması **önceliklendirme** yapar (yine anlayış değil). Üç yanlış şıkkın da gerekçe kısmı "ortak anlayış"tan başka bir çıktıya işaret ediyor.

**Ayırt edici fark:** Konuşmalar, yazılımın nasıl kullanılacağını anlatarak neyin teslim edileceğine dair ortak anlayışı **üretir**; gözden geçirmeler ise zaten yazılmış olan üründeki tutarsızlıkları **tespit eder**.

**Yanılgı etiketi:** `soru-anahtar-ifadesini-atlamak`

---

## Tekrar eden yanılgılar (özet)

| Etiket | Sorular | Ne yapmalı |
|---|---|---|
| `hata-tahmini-kesif-testi-karisikligi` | A-27, C-26 | Üç tecrübeye dayalı tekniği "girdi" üzerinden ayır: keşif = önceden liste YOK (oturumda öğrenerek), hata tahmini/kusur saldırısı = önceden **hata listesi** VAR, kontrol listesi = önceden **test koşulu listesi** VAR. |
| `ifade-dal-kapsami-karisikligi` | C-24 | Kapsam öğesi sorularında önce "öğe nedir?" diye sor: komut testi → çalıştırılabilir komut; dal testi → grafikteki her kenar (koşullu + **koşulsuz**). |
| `kontrol-listesi-ogesi-vs-cikis-kriteri` | B-27 | Bir madde otomatik ölçülebilen bir eşik ise (%X kapsam), o bir çıkış kriteridir; kontrol listesine girmez. |
| `kontrol-listesi-ust-seviye-varyasyon` | C-27 | Kontrol listesinin kapsam avantajı **üst seviye** olmasından gelir; bedeli düşük tekrarlanabilirliktir. |
| `beyaz-kutu-kapsam-olcusunun-amaci` | C-25 | Beyaz kutu kapsam ölçüsü = kara kutu test setinin yeterliliğini objektif ölçme aracı. |
| `senaryo-odakli-vs-kural-odakli-kabul-kriteri` | C-28 | Senaryo odaklı = doğal dilde Given/When/Then; kod ≠ kabul kriteri; "…meli" kuralları = kural odaklı. |
| `soru-anahtar-ifadesini-atlamak` | D-28 (ayrıca C-25'te de görülüyor) | Şıkların gerekçe kısmını sorunun anahtar ifadesiyle (ör. "ortak anlayış", "kara kutuyu destekleme") eşleştir; kendi başına doğru ama soruyla ilgisiz şıklar en sık tuzaktır. |

## Bölüm 5 — Test Planlama ve Risk Yönetimi  (13 soru)

### A-30 · FL-5.1.2 · K1
**Senin cevabın:** d · **Doğru cevap:** c

**Neyi soruyor:** Test uzmanının döngü (iterasyon) ve sürüm planlamasına yaptığı katkının ne olduğunu soruyor. Yani syllabus'un 5.1.2'de saydığı katkı listesinin bilgi düzeyinde hatırlanması isteniyor.

**Doğru şık neden doğru:** Syllabus, test uzmanının hem sürüm hem de döngü planlamasındaki görevlerini açıkça listeler ve bu listenin başında risk analizine katılım gelir. Sürüm planlamasında:

> ALINTI: "sürecine katılır (bkz. bölüm 4.5), proje ve kalite riski analizlerinde görev alır (bkz. bölüm 5.2), kullanıcı"

Döngü planlamasında ise:

> ALINTI: "planlamasında yer alan test uzmanları, kullanıcı hikayelerine ilişkin detaylı bir risk analizine katılır"

Yani "kullanıcı hikayelerinin ayrıntılı risk tanımlaması ve risk değerlendirmesi" (şık c) tam olarak syllabus'un cümlesinin karşılığıdır. Ek olarak risk analizinin iki bileşeni de syllabus'ta risk belirleme + risk değerlendirmesi olarak tanımlıdır, bu da c şıkkının "risk tanımlama ve risk değerlendirme" ifadesini birebir destekler.

**Senin şıkkın neden yanlış:** d şıkkı iki noktadan hatalı. Birincisi, "erken test tasarımı" syllabus'un sürüm/döngü planlaması katkı listesinde yer almaz; oradaki maddeler risk analizi, test edilebilirliğin belirlenmesi, görevlere ayırma, efor tahmini ve test yaklaşımının belirlenmesidir. İkincisi ve daha kritiği, d "yüksek kaliteli yazılımın yayınlanmasını GARANTİ eder" diyor — test, kalite hakkında bilgi sağlar, kaliteyi garanti etmez. ISTQB'de "garanti eder / kanıtlar / sağlar" gibi mutlak ifadeler taşıyan şıklar neredeyse her zaman çeldiricidir.

**Ayırt edici fark:** c, test uzmanının planlamadaki gerçek katkısını (risk belirleme ve değerlendirmesine katılım) tarif eder; d ise listede olmayan bir faaliyeti, üstelik testin veremeyeceği bir "garanti" iddiasıyla birleştirir.

**Yanılgı etiketi:** `mutlak-ifadeli-celdirici-garanti`

---
### A-31 · FL-5.1.3 · K2
**Senin cevabın:** c · **Doğru cevap:** c,e
**Durum:** KISMİ DOĞRU — iki doğru şıktan birini bulmuşsun.

**Neyi doğru yakaladın:** c şıkkını (tahmin edilen hata yoğunluğuna ulaşılması) doğru işaretlemişsin. Bu, syllabus'taki "bütünlük ölçüleri" grubundaki tipik çıkış kriterlerinden biridir:

> ALINTI: "Tipik çıkış kriterleri arasında şunlar yer alır: bütünlük ölçüleri (ör. ulaşılan kapsam seviyesi, çözülmemiş"

Yani hata yoğunluğu ölçüsünün belirlenen hedefe ulaşması bir aktivitenin tamamlandığını göstermek için kullanılabilir. Bunu doğru saptamışsın.

**Eksik kalan doğru şık (e) neden doğru:** Syllabus çıkış kriterlerinin ikinci grubunu "ikili evet/hayır kriterleri" olarak tanımlar ve regresyon testlerinin otomatikleştirilmesini bu grubun örneği olarak DOĞRUDAN sayar:

> ALINTI: "testler koşturuldu, statik test yapıldı, bulunan tüm hatalar raporlandı, tüm regresyon testleri otomatik hale"

(Cümlenin devamı "getirildi" ile biter.) Yani "Regresyon testlerinin otomatize edilmesi" syllabus'ta kelimesi kelimesine geçen bir çıkış kriteri örneğidir; ezberlenmesi gereken bir maddedir.

**Diğer şıklar neden yanlış:** a (test ortamının hazır olması) ve b (test uzmanının test nesnesine login olabilmesi) tipik GİRİŞ kriterleridir — sırasıyla "kaynak elverişliliği" ve "test nesnesinin başlangıç kalite seviyesi (ör. tüm duman testleri geçmiştir)" kategorilerine girer:

> ALINTI: "Tipik giriş kriterleri arasında şunlar yer alır: kaynak elverişliliği (ör. insanlar, araçlar, ortamlar, test verisi,"

d (gereksinimlerin given/when/then formatında yazılması) ise test çalışma ürünlerinin elverişliliğiyle ilgili bir giriş kriteri / Hazır Tanımı öğesidir, çıkış kriteri değildir.

**Ayırt edici fark:** Giriş kriteri bir aktiviteye BAŞLAMAK için gereken önkoşuldur; çıkış kriteri aktivitenin BİTTİĞİNİ gösteren ölçü veya evet/hayır maddesidir — e şıkkı ikincisinin syllabus'ta adı geçen örneğidir.

**Yanılgı etiketi:** `cikis-kriteri-listesi-eksik-hatirlama`

---
### A-33 · FL-5.1.5 · K3
**Senin cevabın:** d · **Doğru cevap:** a

**UYARI:** tablo yapısı metin çıkarımında kaybolmuş, analiz sınırlı — "Öncelik" sütunundaki sayısal değerler metne hiç aktarılmamış. Bağımlılık sütunu okunabilir durumda, öncelik sütunu değil. Bu nedenle önceliğe dayalı seçim adımı doğrulanamıyor, tahmin yürütmüyorum.

**Neyi soruyor:** Öncelik + bağımlılık kısıtı altında test senaryolarının koşum sırasını kurmayı ve ÜÇÜNCÜ koşulacak senaryoyu belirlemeyi istiyor (K3 uygulama).

**Doğru şık neden doğru — adım adım (bağımlılık kısmı metinden türetilebiliyor):**
1. Metinden okunabilen bağımlılıklar: TS 001 → hiçbiri; TS 002 → TS 001; TS 003 → TS 002; TS 004 → TS 002; TS 005 → TS 002.
2. Kural: bir senaryo, bağımlı olduğu senaryo koşulmadan koşulamaz. Syllabus bunu açıkça söyler:
   > ALINTI: "senaryosuna bağımlıysa önce düşük öncelikli test senaryosu koşturulmalıdır."
3. Adım 1 (1. sıra): Yalnızca TS 001 bağımsızdır → **TS 001 birinci**.
4. Adım 2 (2. sıra): TS 001 koşulunca sadece TS 002'nin bağımlılığı çözülür → **TS 002 ikinci**.
5. Adım 3 (3. sıra): TS 002 koşulunca TS 003, TS 004 ve TS 005 aynı anda serbest kalır. Bu üçü arasında seçim ARTIK bağımlılıkla değil, ÖNCELİKLE yapılır (küçük sayı = yüksek öncelik). Resmî cevabın a) TS 003 olması, tabloda TS 003'ün bu üçlü içinde en yüksek önceliğe (en küçük sayıya) sahip olduğunu gösterir. Öncelik sütunu metne aktarılmadığı için bu son adımı sayısal olarak doğrulayamıyorum.
6. Sonuç: sıra TS 001 → TS 002 → **TS 003**.

Yöntemin syllabus dayanağı:

> ALINTI: "İdeal olarak test senaryoları, yukarıdaki önceliklendirme stratejilerinden biri kullanılarak öncelik"

(cümle "seviyelerine göre çalıştırılacak şekilde sıralanır." diye devam eder) — yani önce öncelik sırası kurulur, sonra bağımlılıklar bu sırayı zorunlu olarak bozar.

**Senin şıkkın neden yanlış:** d) TS 001 senin cevabın; ama TS 001 zincirin BİRİNCİ elemanıdır, üçüncüsü değil. Bu, sıralama sorularında en sık görülen iki hatadan birinden çıkar: (i) "hangisi üçüncü koşulmalı" sorusunu "hangisi ilk koşulmalı / en yüksek öncelikli hangisi" diye okumak, ya da (ii) TS 001'in öncelik değerine bakıp (muhtemelen 1) bunu "sıra numarası" sanmak. Öncelik değeri bir sıra numarası değildir; sıra, öncelik + bağımlılık birlikte uygulanarak türetilir.

**Ayırt edici fark:** TS 001 bağımsız olduğu için 1. sırada koşulur; TS 003 ise TS 002'nin bağımlılığı çözüldükten sonra serbest kalan üçlü içinde en yüksek öncelikli olduğu için 3. sırada koşulur.

**Yanılgı etiketi:** `siralama-sorusunda-ordinal-atlama`

---
### B-30 · FL-5.1.3 · K2
**Senin cevabın:** b · **Doğru cevap:** a

**Neyi soruyor:** DevOps teslimat hattında (2) numaralı adım — "kodu sürüm kontrolüne gönderme ve test dalıyla birleştirme" — için EN UYGUN giriş kriterinin hangisi olduğunu soruyor. Yani adım BAŞLAMADAN ÖNCE sağlanması gereken önkoşulu seçmek gerekiyor.

**Doğru şık neden doğru — adım adım:**
1. Giriş kriterinin tanımı:
   > ALINTI: "Giriş kriterleri belirli bir aktivite için önkoşulları tanımlar."
2. Önkoşul, aktivite BAŞLAMADAN ÖNCE değerlendirilebilir olmalıdır. Aktiviteyi yaptıktan sonra ölçülebilen hiçbir şey o aktivitenin giriş kriteri olamaz.
3. Adım (2)'ye girmeden hemen önce elimizde ne var? Sadece adım (1)'in çıktısı: geliştirilmiş kod. Kod üzerinde koşturmadan (statik olarak) yapılabilen kontrol statik analizdir.
4. a) "Statik analiz, gönderilen kod için yüksek önem derecesine sahip uyarılar vermez." — kod yazıldıktan sonra, gönderim/birleştirmeden önce ölçülebilir; test nesnesinin başlangıç kalite seviyesini garanti eden klasik bir giriş kriteridir. Syllabus giriş kriterleri arasında "test nesnesinin başlangıç kalite seviyesi"ni sayar:
   > ALINTI: "Tipik giriş kriterleri arasında şunlar yer alır: kaynak elverişliliği (ör. insanlar, araçlar, ortamlar, test verisi,"

   (cümlenin devamı "... ve test nesnesinin başlangıç kalite seviyesi (ör. tüm duman testleri geçmiştir)" şeklindedir.)
5. Sonuç: **a**.

**Senin şıkkın neden yanlış:** b) "Sürüm kontrolü, kodu test dalıyla birleştirirken çakışma bildirmez." Bu ifade ancak birleştirme DENENDİKTEN sonra bilinebilir — yani adım (2)'nin kendisini yaptıktan sonra ortaya çıkan bir sonuçtur. Dolayısıyla bu bir giriş kriteri değil, adım (2)'nin ÇIKIŞ kriteri (veya doğrudan sonucu) olur. Hatalı adım: "adımın başarıyla tamamlanmış olması" ile "adıma başlayabilmek için gereken önkoşul"u aynı şey saymak.

Diğer çeldiriciler de aynı zaman ekseni hatasını farklı yerlerde yapar: c) "Bileşen testleri derlenir ve koşulmaya hazırlanır" adım (3)'ün giriş kriteridir; d) "Komut kapsamı en az %80" adım (3)'ün ÇIKIŞ kriteridir (bütünlük ölçüsü).

**Ayırt edici fark:** a, adım (2)'ye girmeden önce koda bakarak doğrulanabilir; b ancak adım (2) icra edildikten sonra doğrulanabilir, dolayısıyla önkoşul olamaz.

**Yanılgı etiketi:** `giris-cikis-kriteri-zaman-ekseni-karisikligi`

---
### B-31 · FL-5.1.4 · K3
**Senin cevabın:** a · **Doğru cevap:** b

**Neyi soruyor:** Oranlara dayalı tahminleme (ratio-based estimation) tekniğinin uygulanmasını istiyor: dört geçmiş projenin ORTALAMA verilerinden bir test/geliştirme oranı çıkar, bu oranı yeni projenin geliştirme eforuna uygula.

**Doğru şık neden doğru — adım adım hesap:**
1. Tekniğin tanımı:
   > ALINTI: "edinilen rakamlar toplanır ve bu da benzer projeler için "standart" oranların elde edilmesini mümkün kılar."
2. Soru "dört geçmiş projeden hem geliştirme eforu hem de test eforu için ORTALAMA verileri kullanarak" oranı hesaplamanı söylüyor. Yani önce iki ortalama, sonra oran.
3. Ortalama geliştirme eforu = (800.000 + 1.200.000 + 600.000 + 1.000.000) / 4 = 3.600.000 / 4 = **900.000 $**
4. Ortalama test eforu = (40.000 + 130.000 + 70.000 + 120.000) / 4 = 360.000 / 4 = **90.000 $**
5. Test–geliştirme oranı = 90.000 / 900.000 = **0,10** (yani 1:10, %10)
6. Yeni projeye uygula: 800.000 $ × 0,10 = **80.000 $** → şık **b**.
7. Syllabus'un örneği tam olarak bu mekaniği gösterir:
   > ALINTI: "projede geliştirme eforunun 600 kişi-gün olması bekleniyorsa test eforunun 400 kişi-gün olacağı tahmin"

   (3:2 oranı × 600 kişi-gün = 400 kişi-gün. Bizim durumumuzda 1:10 oranı × 800.000 $ = 80.000 $.)

**Senin şıkkın neden yanlış:** a) 40.000 $ — bu hesaplanmış bir değer değil, tablodaki P1 projesinin test eforunun aynen kopyalanmış hali. Muhtemel hatalı adım: yeni projenin geliştirme eforu 800.000 $ olduğu için, tabloda geliştirme eforu 800.000 $ olan TEK projeyi (P1) bulup onun test eforunu doğrudan cevap yazmak. Bu, "benzer tek bir projeyi eşleştirme" yaklaşımıdır; oranlara dayalı tahminleme değildir. Teknik, tek bir projeye değil, birden çok geçmiş projeden çıkarılan STANDART ORANA dayanır — zaten soru da açıkça "dört geçmiş projeden ... ortalama verileri kullanarak" diyor. P1'in kendi oranı (40/800 = %5) örneklemin en düşük değeridir, yani bu kestirme yol sistematik olarak düşük tahmin üretir.

Diğer çeldiriciler: c) 81.250 $ ve d) 82.500 $, ortalamalar yerine oranların ortalamasını alma / ağırlıklandırmayı karıştırma gibi ara hatalardan üretilmiş sayılardır.

**Ayırt edici fark:** b, dört projenin ortalamalarından türetilen %10'luk standart oranın uygulanmasıdır; a ise hiç oran hesaplamadan tek bir geçmiş projenin test eforunun kopyalanmasıdır.

**Yanılgı etiketi:** `oran-bazli-tahminde-ortalama-yerine-tek-proje`

---
### B-32 · FL-5.1.5 · K3
**Senin cevabın:** c · **Doğru cevap:** b

**UYARI:** tablo yapısı metin çıkarımında kaybolmuş, analiz sınırlı — "Öncelik (1 = daha yüksek öncelik)" sütunundaki sayılar metne hiç aktarılmamış; sadece TC1–TC7 etiketleri ve açıklamaları kalmış. Öncelik değerleri olmadan sıralama sayısal olarak doğrulanamaz, tahmin yürütmüyorum. Mantıksal bağımlılıklar ise metinde eksiksiz duruyor.

**Neyi soruyor:** Yedi test senaryosunu önceliğe göre, ancak mantıksal bağımlılıklara uyarak sıralamayı ve DÖRDÜNCÜ koşulacak senaryoyu bulmayı istiyor.

**Doğru şık neden doğru — türetilebilen kısım:**
1. Bağımlılık kuralları (metinden okunabiliyor): ARA → GÖRÜNTÜLE → EKLE → SİPARİŞ.
2. Bu kurallar İKİ ayrı ürün için paralel iki zincir üretir:
   - A zinciri: TC1 (ARA A) → TC3 (GÖRÜNTÜLE A) → TC5 (EKLE A)
   - B zinciri: TC2 (ARA B) → TC4 (GÖRÜNTÜLE B) → TC6 (EKLE B)
   - TC7 (SİPARİŞ VER) en az bir EKLE testinden sonra gelir.
3. Kritik nokta: bu iki zincir birbirinden bağımsızdır. Yani sıralama tek bir zincirin baştan sona koşulması DEĞİLDİR; iki zincir öncelik değerlerine göre birbirine geçmeli (interleaved) koşulur. Syllabus önce önceliğe göre sıralamayı, sadece bağımlılık zorladığında sapmayı söyler:
   > ALINTI: "Yüksek öncelikli bir test senaryosu düşük öncelikli bir test"
   > ALINTI: "senaryosuna bağımlıysa önce düşük öncelikli test senaryosu koşturulmalıdır."
4. Resmî cevabın b) TC1 olması, ilk üç sırayı bir zincirin (öncelikleri daha yüksek olan zincirin) doldurduğunu, TC1'in ise 4. sıraya düştüğünü gösterir. Öncelik sütunu metinde olmadığı için hangi zincirin önde olduğunu sayısal olarak doğrulayamıyorum.

**Senin şıkkın neden yanlış:** c) TC7. Bu cevap, iki paralel zinciri tek bir zincir sanmaktan çıkar: TC1 (ARA) → TC3 (GÖRÜNTÜLE) → TC5 (EKLE) → TC7 (SİPARİŞ) diye sayarsan 4. eleman TC7 olur. Ancak bu sayım TC2, TC4, TC6'yı — yani B ürününün tüm zincirini — hiç hesaba katmaz ve öncelik değerlerini tamamen yok sayar. Ayrıca TC7 (SİPARİŞ VER) yedi testin son halkasıdır; toplam 7 test varken onun 4. sırada olması, kalan üç testin hepsinin SİPARİŞ'ten sonra koşulması demektir ki bu bağımlılık mantığına aykırıdır.

**Ayırt edici fark:** Doğru çözüm, iki ürün zincirini öncelik sırasına göre iç içe geçirir ve TC1'i 4. sıraya iter; senin çözümün ise tek bir fonksiyonel akışı baştan sona takip edip 4. adımı "SİPARİŞ" olarak okur.

**Yanılgı etiketi:** `paralel-bagimlilik-zincirlerini-tek-zincir-sanma`

---
### B-34 · FL-5.2.4 · K2
**Senin cevabın:** b · **Doğru cevap:** c

**Neyi doğru yakaladın:** 1↔B (etkin olmayan döngü → performans testi) ve 4↔C (belirli yaşın üzerindeki hastalar → sınır değer analizi) eşleşmelerini DOĞRU yapmışsın. Hata sadece 2 ve 3'ün yer değiştirmesinde.

**Neyi soruyor:** Dört riski, en uygun risk yanıtı/azaltma faaliyetiyle eşleştirmeyi istiyor. Burada iki tür ayrım aynı anda gerekiyor: (i) ürün riski mi proje/dış risk mi, (ii) risk yanıtı hangisi (test yoluyla azaltma / kabul / transfer).

**Doğru şık neden doğru — adım adım:**
1. Syllabus'un risk yanıtı seçenekleri:
   > ALINTI: "mümkündür;  örneğin,  test  yoluyla  riskin  azaltılması,  risk  kabulü,  risk  transferi  veya  acil  durum  planı"
2. **Risk 1 — Etkin olmayan döngü uygulamasının uzun sistem yanıtlarına neden olması → B (Performans testi).** Bu bir ÜRÜN riskidir; syllabus ürün riski örneklerinde birebir geçer:
   > ALINTI: "riski örnekleri arasında şunlar yer alır: eksik ya da yanlış fonksiyonalite, hatalı hesaplamalar, çalışma"

   (devamı: "...zamanı hataları, zayıf mimari, etkin olmayan algoritmalar, yetersiz yanıt süresi..."). Yanıt süresi riskinin karşılığı performans testidir:
   > ALINTI: "Etkilenen kalite karakteristiklerini hedefleyen uygun test çeşitlerini uygulamak."
3. **Risk 2 — Tüketicilerin tercihlerini değiştirmesi → A (Risk kabulü).** Bu pazar/iş riskidir; ne test edilebilir, ne başkasına devredilebilir, ne de sigortalanabilir. Ekibin kontrolü dışındadır, dolayısıyla tek makul yanıt kabuldür.
4. **Risk 3 — Sunucu odasını su basması → D (Risk transferi).** Bu fiziksel/tesis kaynaklı bir risktir; klasik transfer yanıtı sigortalamak ya da barındırmayı üçüncü tarafa (veri merkezi/bulut sağlayıcı) devretmektir. Test ederek azaltılamaz.
5. **Risk 4 — Belirli bir YAŞIN ÜZERİNDEKİ hastaların hatalı rapor alması → C (Sınır değer analizi).** "Belirli bir yaşın üzerinde" ifadesi bir eşik/sınır tanımlar; eşik etrafındaki hatalar tam olarak sınır değer analizinin hedefidir:
   > ALINTI: "Uygun test teknikleri ve kapsam seviyeleri uygulamak"
6. Sonuç: 1B, 2A, 3D, 4C → şık **c**.

**Senin şıkkın neden yanlış:** b) 1B, 2D, 3A, 4C. 1 ve 4 doğru; ancak 2'ye transfer, 3'e kabul atamışsın — tam ters. Hatalı adım: "risk transferi"ni "kontrolüm dışındaki risk" ile eşitlemek. Transfer, riskin sonucunu (finansal yükünü) sözleşmeyle veya sigortayla BAŞKA BİR TARAFA devredebildiğin durumlarda geçerlidir; kabul ise devredilemeyen ama katlanılabilir riskler içindir. Tüketici tercihindeki değişimi devralacak bir taraf yoktur (→ kabul); su baskınının maliyetini devralacak bir sigortacı/barındırma sağlayıcı vardır (→ transfer).

**Ayırt edici fark:** Transfer, riskin maliyetini üstlenecek bir karşı tarafın bulunabildiği durumlarda (su baskını → sigorta); kabul ise böyle bir karşı tarafın olmadığı, riskin bilinçli olarak üstlenildiği durumlarda (pazar tercihleri) uygulanır.

**Yanılgı etiketi:** `risk-yaniti-kabul-transfer-karisikligi`

---
### C-32 · FL-5.1.5 · K3
**Senin cevabın:** c · **Doğru cevap:** a

**UYARI:** tablo/şekil yapısı metin çıkarımında kaybolmuş, analiz sınırlı — soru bir ŞEKLE dayanıyor (öncelik değerleri kutularda, bağımlılıklar oklarla). Metin çıkarımında şeklin tamamı kaybolmuş: ne öncelik değerleri ne de oklar mevcut. Yalnızca örnek olarak verilen tek bir bağımlılık (TC 4 → TC 5) okunabiliyor. Sıralamayı türetmek için gereken veri yok; tahmin yürütmüyorum.

**Neyi soruyor:** Öncelik değerleri ve bağımlılık okları verilmiş 7 test senaryosu için koşum çizelgesini kurup 6. sırada koşulacak senaryoyu bulmayı istiyor (K3).

**Uygulaman gereken yöntem (bu soru tipini gelecekte çözmek için):**
1. Tüm senaryoları öncelik değerine göre sırala (1 = en yüksek).
2. Listeyi baştan tara; her adımda, bağımlılıkları HALİHAZIRDA koşulmuş olan senaryolar arasından en yüksek öncelikliyi seç.
3. Bağımlılığı henüz karşılanmamış yüksek öncelikli bir senaryo varsa, onu atla ve bağımlı olduğu düşük öncelikli senaryoyu önce koş:
   > ALINTI: "Yüksek öncelikli bir test senaryosu düşük öncelikli bir test"
   > ALINTI: "senaryosuna bağımlıysa önce düşük öncelikli test senaryosu koşturulmalıdır."
4. Bu adımı 7 kez tekrarlayarak tam sırayı yaz, sonra soruda istenen ordinali (burada 6.) oku. Kısayol yapma — sorulan sıra 6. bile olsa 1'den 6'ya kadar tüm listeyi yazmak, ordinal atlamasını (bkz. A-33) engelleyen en güvenli yoldur.
5. Genel ilke:
   > ALINTI: "İdeal olarak test senaryoları, yukarıdaki önceliklendirme stratejilerinden biri kullanılarak öncelik"

**Senin şıkkın neden yanlış:** Şekil verisi olmadan b) TC 5'i seçmene yol açan spesifik adımı belirleyemiyorum. Ancak bu soru tipinde yaptığın hata deseni A-33 ve B-32 ile aynı yönde: sıralamayı sonuna kadar açıkça yazmadan, kısmi zincire bakarak ordinali tahmin etmek. Resmî cevap a) TC 3'tür.

**Ayırt edici fark:** Şekil verisi kayıp olduğu için bu soruda kesin ayrım belirtilemez; yöntem hatası düzeyinde ayrım, tam sıra listesini yazmak ile kısmi zincirden ordinal okumak arasındadır.

**Yanılgı etiketi:** `siralama-sorusunda-ordinal-atlama`

---
### C-33 · FL-5.1.6 · K1
**Senin cevabın:** c · **Doğru cevap:** b

**Neyi soruyor:** Test piramidi modelinin NE gösterdiğini, yani modelin tanımını soruyor. Saf hatırlama (K1) sorusu.

**Doğru şık neden doğru:** Syllabus'un 5.1.6 bölümünün ilk cümlesi sorunun cevabını birebir verir:

> ALINTI: "Test piramidi, farklı testlerin farklı ayrıntıları olabileceğini gösteren bir modeldir."

"Farklı ayrıntılar" = farklı ayrıntı düzeyi (granularity) → şık **b**. Katmanlar arasındaki ayrım da tam olarak bu eksende tanımlanır:

> ALINTI: "yüksekse test ayrıntısı, test izolasyonu o kadar düşük, test koşumu süresi ise o kadar yüksek olur."

Yani piramidin alt katmanı küçük/izole/hızlı testleri (ince ayrıntı), üst katmanı ise uçtan uca testleri (kaba ayrıntı) temsil eder.

**Senin şıkkın neden yanlış:** c) "Testlerin farklı kapsam kriterleri gerektirebileceğini." Kapsam (coverage) piramidin tanımlayıcı ekseni değildir. Syllabus kapsamdan piramit bağlamında yalnızca bir sonuç olarak söz eder: alt katmanda makul kapsam için ÇOK SAYIDA test gerekir, üst katmanda ise BİRKAÇ test yeter. Yani kapsam, ayrıntı düzeyinin bir sonucudur, modelin gösterdiği şeyin kendisi değil. c şıkkı bu ikincil gözlemi model tanımının yerine koyuyor.

Diğer çeldiriciler farklı 5.1 konularının tanımlarıdır: a (farklı öncelikler) ve d (testlerin diğer testlere bağlı olması) 5.1.5 test senaryosu önceliklendirme konusuna aittir, piramide değil.

**Ayırt edici fark:** Test piramidinin ekseni test AYRINTI DÜZEYİDİR (izolasyon ve koşum süresiyle birlikte değişen); kapsam kriteri ise bu ayrıntı düzeyinin yan sonucudur, modelin gösterdiği şey değildir.

**Yanılgı etiketi:** `test-piramidi-ayrinti-yerine-kapsam`

---
### C-34 · FL-5.1.7 · K2
**Senin cevabın:** a · **Doğru cevap:** d

**Neyi soruyor:** Test çeyrekleri ile test seviyeleri ve test türleri arasındaki ilişkinin ne olduğunu soruyor.

**Doğru şık neden doğru:** Syllabus test çeyreklerini bir GRUPLAMA modeli olarak tanımlar:

> ALINTI: "yazılım geliştirmede uygun test çeşitleri, aktiviteleri, test teknikleri ve iş ürünleri ile gruplandırır."

Gruplamanın hangi kriterlere göre yapıldığı da açıkça verilir — iş odaklı/teknoloji odaklı ekseni doğrudan hedeflenen paydaş kitlesine karşılık gelir:

> ALINTI: "Bu modelde testler iş odaklı veya teknoloji odaklı olabilir."

Ve modelin paydaş boyutu:

> ALINTI: "paydaşlara test çeşitlerinin ayrımını yapmanın ve açıklamanın bir yolunu sunar."

Yani d) "test seviyelerini ve test türlerini belirli paydaşları hedefleme gibi çeşitli kriterlere göre gruplandırır" ifadesi syllabus'un iki eksenli (iş/teknoloji odaklı × ekibi destekleme/ürünü eleştirme) gruplama tanımının doğru özetidir.

**Senin şıkkın neden yanlış:** a) "belirli kombinasyonlarını temsil eder ve yazılım geliştirme yaşam döngüsündeki KONUMLARINI tanımlar." İki hata var. Birincisi, çeyrekler zaman ekseninde bir konum/sıra tanımlamaz — Q1'den Q4'e giden bir kronolojik akış yoktur; Q1–Q4 numaralandırması bir aşama sırası değil, sadece dört kutunun etiketidir. İkincisi, çeyrekler "belirli kombinasyonları" (sabit, bire bir eşleşmeler) değil, esnek gruplamalar sunar. Syllabus modelin faydasını YGYD'deki konumlandırma olarak değil, "tüm uygun test çeşitlerinin ve test seviyelerinin YGYD'ne dahil edilmesini SAĞLAMAK" olarak tanımlar — yani kapsayıcılığı görselleştirmek, sırayı belirlemek değil.

**Ayırt edici fark:** Çeyrekler, testleri paydaş odağı ve amaç eksenlerine göre GRUPLAR (d); YGYD üzerinde bir zaman/aşama KONUMU atamaz (a).

**Yanılgı etiketi:** `test-ceyrekleri-test-seviyesi-karisikligi`

---
### C-35 · FL-5.2.3 · K2
**Senin cevabın:** d · **Doğru cevap:** c

**Neyi soruyor:** Ürün riski analizinin testlerin TİTİZLİĞİNİ (rigor) ve KAPSAMINI nasıl etkileyebileceğine dair bir ÖRNEK istiyor. Yani soru, FL-5.2.3 öğrenme hedefinin tam metnine kilitli: etkinin nereye yansıdığı sorulmuş.

**Doğru şık neden doğru:** Syllabus'un bu bölümdeki başlık cümlesi öğrenme hedefiyle birebir örtüşür:

> ALINTI: "Ürün riski analizi, testlerin bütünlüğünü ve kapsamını etkileyebilir. Sonuçları aşağıdaki amaçlarla kullanılır:"

Bu cümlenin hemen ardından gelen madde, değerlendirilen risk seviyesinin testin ne kadar titiz olacağını (hangi teknik, ne düzeyde kapsam) belirlediğini söyler:

> ALINTI: "Kullanılacak test tekniklerini ve ulaşılacak kapsamı belirlemek"

Risk seviyesinin bu kararın girdisi olduğu da açıktır:

> ALINTI: "Bu iki faktör bir risk ölçüsü olan risk seviyesini belirtir. Risk seviyesi ne kadar yüksekse çözülmesi de o"

(devamı "kadar önemlidir.") Adım adım: risk olasılığı × risk etkisi → risk seviyesi → yüksek risk seviyesindeki alanlarda daha titiz teknikler ve daha yüksek kapsam hedefi. Bu tam olarak c) "Değerlendirilen risk seviyesi, testlerin kesinliğini (rigor) seçmemize yardımcı olur."

**Senin şıkkın neden yanlış:** d) "Risk analizi, kapsam öğelerini türetmemizi sağlar." Kapsam öğeleri (coverage items) risk analizinden DEĞİL, test esasından türetilen test koşullarına test tasarım tekniklerinin uygulanmasıyla elde edilir (bkz. bölüm 1.4 / bölüm 4). Risk analizi kapsam ÖĞELERİNİ üretmez; hangi teknikle çalışılacağını ve ne KADAR kapsama ulaşılacağını, yani kapsamın DÜZEYİNİ belirler. Hatalı adım: "kapsam düzeyini belirlemek" ile "kapsam öğesini türetmek"i eş anlamlı saymak — biri yönetsel bir hedef kararı, diğeri teknik bir tasarım çıktısıdır.

Diğer çeldiriciler doğru ifadelerdir ama soruyu cevaplamazlar: a) risk gözetimini (5.2.4), b) risk azaltmayı (5.2.4) tarif eder; hiçbiri testin titizliği/kapsamı üzerindeki etkiye örnek değildir.

**Ayırt edici fark:** c, risk seviyesinin testin titizlik DÜZEYİNİ seçtiğini söyler (5.2.3'ün konusu); d ise kapsam öğelerinin ÜRETİMİNİ risk analizine bağlar, oysa bu test analizi ve test tasarımının işidir.

**Yanılgı etiketi:** `risk-analizi-kapsam-ogesi-turetme-yanilgisi`

---
### D-32 · FL-5.1.5 · K3
**Senin cevabın:** d · **Doğru cevap:** b

**UYARI:** tablo yapısı metin çıkarımında kaybolmuş, analiz sınırlı — izlenebilirlik matrisinin satır-sütun ilişkisi tamamen bozulmuş. Metinde önce Ger1–Ger7 etiketleri, sonra iki "X", sonra TS1–TS4 etiketleri, sonra yedi "X" arka arkaya çıkmış. Hangi X'in hangi (TS, Ger) hücresine ait olduğu belirlenemiyor; toplam X sayısı bile (9) dört senaryo × yedi gereksinim ızgarasına güvenilir şekilde yerleştirilemiyor. Tahmin yürütmüyorum.

**Neyi soruyor:** "Ek kapsama önceliklendirmesi" (additional coverage prioritization) tekniğini izlenebilirlik matrisine uygulayıp EN SON koşulacak senaryoyu bulmayı istiyor.

**Uygulaman gereken yöntem — adım adım:**
1. Tekniğin syllabus tanımı:
   > ALINTI: "denilen başka bir varyantta, en yüksek kapsama ulaşan test senaryosu ilk uygulanır; sonraki"
   > ALINTI: "her bir test senaryosu en yüksek ek kapsama ulaşan test senaryosudur."
2. **Adım 1:** Her test senaryosunun kapsadığı gereksinim SAYISINI say. En çok gereksinim kapsayan senaryo 1. sıraya konur.
3. **Adım 2:** Seçilen senaryonun kapsadığı gereksinimleri listeden düş (artık "kapsanmış" sayılırlar).
4. **Adım 3:** Kalan senaryolar için, HENÜZ KAPSANMAMIŞ gereksinimlerden kaç tanesini eklediklerini yeniden say. Toplam kapsam değil, EK kapsam sayılır — bu tekniğin can alıcı noktasıdır.
5. **Adım 4:** En yüksek ek kapsamı getireni sonraki sıraya koy; adım 3–4'ü tekrarla.
6. **Sonuç:** EN SON kalan senaryo, kendinden önceki senaryolar tarafından zaten kapsanmış gereksinimlerle en fazla örtüşen, yani en az (çoğu zaman sıfır) YENİ gereksinim ekleyen senaryodur. Resmî cevap b) TS2'dir; matris okunabilir olsaydı TS2'nin gereksinimlerinin diğer üç senaryo tarafından tamamen veya büyük ölçüde zaten kapsandığını görecektin.

**Senin şıkkın neden yanlış:** Matris verisi kayıp olduğundan d) TS4'ü seçmene yol açan spesifik adımı belirleyemiyorum. Bu soru tipinde en sık yapılan hata, adım 3'ü atlayıp senaryoları sadece TOPLAM kapsadıkları gereksinim sayısına göre sıralamak ve "en az X işareti olan en sona gider" diye kestirmeden gitmektir. Bu yanlıştır: az X'i olan bir senaryo, o X'ler başka hiçbir senaryoda yoksa erken sıraya gelebilir; çok X'i olan bir senaryo ise X'lerinin hepsi zaten kapsanmışsa en sona düşebilir. Belirleyici olan mutlak sayı değil, ARTIRIMLI (ek) katkıdır.

**Ayırt edici fark:** Ek kapsama önceliklendirmesinde sıra, her adımda YENİ kapsanan gereksinim sayısına göre yeniden hesaplanır; senaryonun toplam işaret sayısına göre değil.

**Yanılgı etiketi:** `ek-kapsam-yerine-toplam-kapsam-sayma`

---
### D-33 · FL-5.1.7 · K2
**Senin cevabın:** a · **Doğru cevap:** c

**Neyi soruyor:** Test çeyreklerinin test çalışmalarına sağladığı FAYDANIN ne olduğunu soruyor (C-34 ile aynı öğrenme hedefi, farklı açıdan).

**Doğru şık neden doğru:** Syllabus, test çeyreklerinin faydasını iki parça halinde ve c şıkkının iki parçasıyla birebir örtüşecek şekilde verir. Birinci parça — bazı test türlerinin belirli seviyelerle daha alakalı olduğunu göstermek:

> ALINTI: "görselleştirmede ve bazı test çeşitlerinin belirli test seviyeleriyle diğerlerinden daha alakalı olduğunu"

İkinci parça — teknik olmayan paydaşlar dahil herkese test türlerini açıklamak:

> ALINTI: "paydaşlara test çeşitlerinin ayrımını yapmanın ve açıklamanın bir yolunu sunar."

(Bu cümlenin öznesi bir önceki satırdaki "geliştiriciler, test uzmanları ve iş birimleri dahil tüm" ifadesidir — yani teknik olmayan iş birimleri de dahil.) c şıkkı bu iki cümlenin toplamıdır; bu yüzden doğrudur.

**Senin şıkkın neden yanlış:** a) "Test sürecini, dört temel test seviyesine karşılık gelen dört aşamaya ayırarak ... bileşen, entegrasyon, sistem ve kabul testleri." Bu şık, dört çeyreği dört test SEVİYESİYLE eşitliyor. Syllabus'ta böyle bir eşleme yoktur: çeyrekler iş odaklı/teknoloji odaklı ve ekibi destekleme/ürünü eleştirme eksenlerinden doğar, test seviyelerinden değil. Somut karşı örnek: Q1 içinde İKİ test seviyesi birden vardır (bileşen ve bileşen entegrasyon testleri); Q3'te ise kullanıcı kabul testi ile keşif testi ve kullanılabilirlik testi bir arada bulunur — yani bir çeyrek bir seviyeye karşılık gelmez. Ayrıca "dört aşama" ifadesi çeyreklere olmayan bir zaman sırası atfeder. Hatalı adım: "dört" sayısının çeyreklerde ve klasik test seviyelerinde ortak olmasından yola çıkıp ikisini eşleştirmek.

Diğer çeldiriciler: b) düşük seviyeli kapsamdan yüksek seviyeli kapsam çıkarma — syllabus'ta böyle bir iddia yok, üstelik yanlış bir çıkarımdır. d) dört psikolojik tip — model adının çağrıştırdığı tamamen alakasız bir çeldiricidir.

**Ayırt edici fark:** Çeyrekler, test türlerini paydaşlara açıklamaya ve hangi türün hangi seviyeyle daha alakalı olduğunu göstermeye yarar (c); dört çeyrek dört test seviyesine karşılık gelen dört aşama DEĞİLDİR (a).

**Yanılgı etiketi:** `test-ceyrekleri-test-seviyesi-karisikligi`

---

## Tekrar Eden Yanılgı Etiketleri (özet)

| Etiket | Sorular | Not |
|---|---|---|
| `test-ceyrekleri-test-seviyesi-karisikligi` | C-34, D-33 | Test çeyreklerini test seviyeleriyle / YGYD aşamalarıyla eşleştirme. İki soruda da AYNI hata, ikisinde de a şıkkı seçilmiş. En net tekrar eden zayıflık. |
| `siralama-sorusunda-ordinal-atlama` | A-33, C-32 | Tam koşum sırasını yazmadan, kısmi zincirden istenen ordinali okumak. |
| `paralel-bagimlilik-zincirlerini-tek-zincir-sanma` | B-32 | Aynı ailedeki sıralama hatası (A-33, C-32 ile birlikte 4 K3 sorusunun 3'ü sıralama). |
| `ek-kapsam-yerine-toplam-kapsam-sayma` | D-32 | Sıralama ailesinin dördüncü üyesi. |
| `giris-cikis-kriteri-zaman-ekseni-karisikligi` | B-30 | Aktivitenin sonucunu önkoşul sanmak. |
| `cikis-kriteri-listesi-eksik-hatirlama` | A-31 | Syllabus'un ikili evet/hayır çıkış kriteri örnekleri eksik hatırlanmış. |
| `risk-yaniti-kabul-transfer-karisikligi` | B-34 | Kabul ↔ transfer yer değiştirmesi. |
| `risk-analizi-kapsam-ogesi-turetme-yanilgisi` | C-35 | Kapsam düzeyi ≠ kapsam öğesi. |
| `test-piramidi-ayrinti-yerine-kapsam` | C-33 | Piramidin ekseni ayrıntı düzeyi, kapsam değil. |
| `oran-bazli-tahminde-ortalama-yerine-tek-proje` | B-31 | Ortalamadan oran çıkarmak yerine tek benzer projeyi kopyalamak. |
| `mutlak-ifadeli-celdirici-garanti` | A-30 | "Garanti eder" içeren şıkkı seçmek. |

**En kritik iki desen:**
1. **Sıralama/önceliklendirme (FL-5.1.5) K3 soruları** — bu paketteki 4 sorunun (A-33, B-32, C-32, D-32) DÖRDÜNDE de hata var. Ortak kök neden: tam koşum listesini adım adım yazmak yerine kısayol/sezgi kullanmak. Çözüm: her seferinde 1'den N'ye kadar tüm sırayı kağıda yazmak.
2. **Test çeyrekleri (FL-5.1.7)** — 2 sorunun 2'sinde de aynı yönde hata: çeyrekleri test seviyesi/YGYD aşaması sanmak. Çözüm: Q1–Q4'ün iki eksenden (iş↔teknoloji odaklı, ekibi destekle↔ürünü eleştir) doğduğunu, seviye veya zaman sırası olmadığını ezberlemek.

## Bölüm 5 — İzleme, Konfigürasyon ve Hata Yönetimi  (6 soru)

### A-37 · FL-5.4.1 · K2
**Senin cevabın:** a · **Doğru cevap:** c

**Neyi soruyor:** Bir otomatik test betiğini güncellediğinde, test deposunda bu betiğin YENİ BİR SÜRÜMÜNÜN oluştuğunu gösteren/kayıt altına alan disiplinin adı soruluyor. Yani "sürüm/versiyon oluşturma ve kayıt" hangi yönetim disiplinine aittir?

**Doğru şık neden doğru:** Test betiği bir yapılandırma öğesidir; onun benzersiz tanımlanması, versiyon kontrolü ve değişikliklerinin izlenmesi doğrudan yapılandırma yönetiminin görevidir.
> ALINTI: "Test öğeleri de dahil olmak üzere tüm yapılandırma öğelerinin benzersiz olarak tanımlanması,"

Yeni bir sürüm/temel çizgi oluştuğunda kaydı tutan ve gerektiğinde eski sürüme dönmeyi mümkün kılan mekanizma da YY'dir:
> ALINTI: "Yeni bir temel çizgi oluşturulduğunda, yapılandırma yönetimi değiştirilen yapılandırma öğelerinin bir"

> ALINTI: "Önceki test sonuçlarını yeniden üretmek için önceki temel çizgiye geri dönülebilir."

**Senin şıkkın neden yanlış:** "İzlenebilirlik yönetimi" (a), test öğeleri ile gereksinimler/test koşulları/riskler arasındaki BAĞLANTIYI kurma ve takip etme kavramıdır. İzlenebilirlik, yapılandırma yönetiminin sağladığı bir SONUÇTUR, ayrı bir sürüm oluşturma işlemi değildir:
> ALINTI: "böylece test süreci boyunca izlenebilirliğinin sürdürülmesi"

Yani izlenebilirlik "bu betik hangi gereksinimi kapsıyor?" sorusunu cevaplar; "bu betiğin v3'ü depoda oluştu" bilgisini üreten şey değildir.

**Ayırt edici fark:** Yapılandırma yönetimi öğenin SÜRÜMÜNÜ tanımlar/kaydeder; izlenebilirlik ise öğenin başka iş ürünleriyle İLİŞKİSİNİ kurar.

**Yanılgı etiketi:** `konfigurasyon-yonetimi-izlenebilirlikle-karistirma`

---
### C-36 · FL-5.3.2 · K2
**Senin cevabın:** d · **Doğru cevap:** b

**Neyi soruyor:** Test sürecindeki hangi faaliyet, test ilerleme raporlarını EN ÇOK (girdi olarak) kullanır?

**Doğru şık neden doğru:** Testin tamamlanması faaliyeti, proje boyunca üretilmiş tüm test iş ürünlerini toplayıp bir araya getirir ve test tamamlama raporunu doğrudan test ilerleme raporlarına dayandırır.
> ALINTI: "Test tamamlama, test projesinde elde edilen deneyimi, proje boyunca üretilen test çalışma ürünlerini ve"

> ALINTI: "Bu rapor, test ilerleme raporu"

> ALINTI: "Test ilerleme raporuna dayalı test metrikleri"

Yani test tamamlama raporunun içeriği (özet, sapmalar, metrikler) birikmiş ilerleme raporlarından türetilir — bu faaliyet ilerleme raporlarının en yoğun tüketicisidir.

**Senin şıkkın neden yanlış:** "Test planlaması" (d), test yaklaşımını, kaynakları ve zaman çizelgesini BAŞTAN belirleme faaliyetidir; girdisi ağırlıklı olarak test esası, riskler ve organizasyonel test stratejisidir. İlerleme raporları planlamayı ancak DOLAYLI olarak (kontrol yönergeleri yoluyla plan güncellemesi) etkiler; raporun asıl toplandığı ve özetlendiği yer tamamlama faaliyetidir. Test tasarımı (a) ve test analizi (c) ise test esasından test koşulu/senaryosu üreten faaliyetlerdir, ilerleme raporunu girdi olarak kullanmazlar.

**Ayırt edici fark:** Test planlaması ilerleme raporunu düzeltici aksiyon için ARA ARA kullanır; testin tamamlanması ise ilerleme raporlarının TAMAMINI toplayıp tamamlama raporuna dönüştürür.

**Yanılgı etiketi:** `test-ilerleme-raporunun-tuketicisi-karisikligi`

---
### C-37 · FL-5.4.1 · K2
**Senin cevabın:** a · **Doğru cevap:** d

**Neyi soruyor:** Verilen dört ifadeden hangisi yapılandırma yönetiminin testi desteklemesine ÖRNEK DEĞİLDİR (yani başka bir sürece aittir)?

**Doğru şık neden doğru:** d şıkkı ("Tespit edilen tüm hatalara bir durum atanmıştır") yapılandırma yönetiminin değil, HATA YÖNETİMİNİN (bölüm 5.5) alanıdır; "durum" bir hata raporunun alanıdır:
> ALINTI: "Hatanın durumu (ör. açık, ertelenmiş, tekrarlanmış, düzeltilmeyi bekliyor, onaylama testi"

Buna karşılık a, b ve c şıkları syllabus'ta YY'nin sağladığı maddelerle birebir örtüşür:
> ALINTI: "Test öğeleri de dahil olmak üzere tüm yapılandırma öğelerinin benzersiz olarak tanımlanması,"

> ALINTI: "Tanımlanan tüm dokümantasyon ve yazılım öğelerinin test çalışma ürünlerinde açık"

(a = benzersiz tanımlama + versiyon kontrolü; b = test ortamı öğelerindeki değişikliklerin izlenmesi, karmaşık yapılandırma öğesi olarak test ortamı; c = tanımlı öğelerin test iş ürünlerinde açıkça belirtilmesi.)

**Senin şıkkın neden yanlış:** a şıkkı ("Depoya yapılan tüm işlemler benzersiz bir şekilde tanımlanır ve sürüm kontrolüne tabi tutulur") yapılandırma yönetiminin TANIM cümlesinin ta kendisidir — yani soruda aranan "DEĞİLDİR" cevabının tam tersi, en tipik YY örneğidir. Soru olumsuz ("DEĞİLDİR") kurulduğu için en doğru YY örneğini seçmek hatalı olur.

**Ayırt edici fark:** a benzersiz tanımlama + versiyon kontrolü ile YY'nin çekirdek tanımıdır; d ise hata iş akışındaki durum ataması olduğu için 5.5 Hata Yönetimi'ne aittir.

**Yanılgı etiketi:** `hata-raporu-vs-diger-surec-ciktisi-karisikligi`

---
### C-38 · FL-5.5.1 · K3
**Senin cevabın:** a · **Doğru cevap:** b

**Neyi soruyor:** Verilen WebShop hata raporunda EKSİK olan EN ÖNEMLİ bilgi hangisidir? Yani hata raporu içerik listesindeki hangi kalem hem eksik hem de kritik?

**Doğru şık neden doğru:** Raporda test nesnesi (WebShop v0.99), yeniden oluşturma adımları, beklenen/gerçek sonuç, önem derecesi ve öncelik var; ancak TEST ORTAMI hiç yok. Web tabanlı bir uygulamada tarayıcı/işletim sistemi/sürüm bilgisi olmadan hata yeniden üretilemez. Syllabus hata raporu içeriğinde test nesnesi ile test ortamını birlikte zorunlu kalem olarak sayar:
> ALINTI: "Test nesnesinin ve test ortamının tanımı"

Bu maddenin test nesnesi yarısı raporda karşılanmış (c şıkkı bu yüzden eksik değil), test ortamı yarısı ise tamamen boştur.

**Senin şıkkın neden yanlış:** a şıkkı ("Test eden kişinin adı ve tarih") gerçekten de syllabus'un hata raporu içerik listesinde yer alır:
> ALINTI: "Anomalinin gözlemlendiği tarih, bildiren organizasyon ve yazar (rolü de dahil olmak üzere)"

Yani seçimin "hata raporu içeriği" kavramı açısından tamamen alakasız değil — bunu doğru yakalamışsın. Ancak bu alanlar tipik olarak araç tarafından otomatik doldurulan, izlenebilirlik/iletişim amaçlı meta verilerdir ve hatanın yeniden üretilmesi için gerekli değildir:
> ALINTI: "Bu verilerin bir kısmı hata yönetim araçları kullanıldığında otomatik olarak dahil edilebilir (ör. tanımlayıcı,"

Ayrıca d şıkkı (paydaş çıkarları üzerindeki etki) raporda zaten "Önem derecesi: Yüksek" olarak vardır:
> ALINTI: "Hatanın paydaşların çıkarları veya gereksinimler üzerindeki önem derecesi (etki derecesi)"

**Ayırt edici fark:** Ad/tarih hatanın KİM ve NE ZAMAN meta verisidir ve genelde otomatik gelir; test ortamı ve sürüm numaraları ise hatanın NEREDE oluştuğunu belirler ve olmadan hata yeniden üretilemez — bu yüzden eksikliği daha kritiktir.

**Yanılgı etiketi:** `hata-raporu-kritik-alan-onceliklendirme`

---
### D-36 · FL-5.3.2 · K2
**Senin cevabın:** d · **Doğru cevap:** c

**Neyi soruyor:** Dört seçenekten hangisi bir TEST RAPORUNUN geçerli amacı DEĞİLDİR? Yani hangisi test raporunun değil, başka bir dokümanın işidir?

**Doğru şık neden doğru:** c şıkkı ("Her bir hataya ilişkin, örneğin hatayı yeniden üretmek için izlenecek adımlar gibi bilgileri sağlamak") HATA RAPORUNUN içeriğidir, test raporunun değil:
> ALINTI: "Anomaliyi tespit eden test adımları da dahil olmak üzere anomalinin yeniden oluşturulmasını ve"

Test raporu ise tekil hata ayrıntısı değil, özet/iletim aracıdır:
> ALINTI: "Test raporunda test öncesi ve sonrasındaki test bilgileri özetlenir ve iletilir."

**Senin şıkkın neden yanlış:** d şıkkı ("Bir sonraki periyot için planlanan testler hakkında bilgi sunmak") test ilerleme raporunun syllabus'ta AÇIKÇA sayılan içerik maddelerinden biridir — yani tamamen geçerli bir amaçtır:
> ALINTI: "Sıradaki periyod için planlanan testler"

a şıkkı test gözetimi/kontrol amacına, b şıkkı ise raporun temel özetleme amacına karşılık gelir; ikisi de geçerlidir.

**Ayırt edici fark:** Test raporu AGREGE düzeyde ilerleme, metrik, risk ve sonraki periyot bilgisi verir; tek tek hataların yeniden üretim adımları ise HATA RAPORUNA aittir.

**Yanılgı etiketi:** `hata-raporu-vs-diger-surec-ciktisi-karisikligi`

---
### D-38 · FL-5.5.1 · K3
**Senin cevabın:** b · **Doğru cevap:** a

**Neyi soruyor:** Kitap Ödünç Verme Sistemi hata raporunda, geliştiricinin hatayı HIZLI YENİDEN OLUŞTURMASINA en çok hangi ekleme yardım eder?

**Doğru şık neden doğru:** Rapordaki adımlar genel ("bir kullanıcı olarak giriş yapın", "bir kitabın yanındaki düğmeye tıklayın") — hangi kullanıcı, hangi kitap belli değil. Yeniden üretim için hatanın bağlamı ve kullanılan test verisi gerekir:
> ALINTI: "Hatanın bağlamı (ör. çalıştırılan test senaryosu, yapılan test faaliyeti, YGYD aşaması ve test"

> ALINTI: "tekniği, kontrol listesi ve kullanılan test verisi gibi diğer ilgili bilgiler)"

Ve hata raporunun amacı, çözecek kişiye YETERLİ bilgi vermektir:
> ALINTI: "Raporlanan hataları ele almaktan ve çözmekten sorumlu olanlara sorunu çözmek için yeterli"

Etkilenen kullanıcıların/kitapların belirtilmesi, geliştiricinin aynı veri kümesiyle senaryoyu birebir tekrar etmesini sağlar.

**Senin şıkkın neden yanlış:** b şıkkı ("Öncelik" alanındaki eksik değerin doldurulması) gerçekten raporun eksik bir alanıdır ve syllabus'ta yer alır:
> ALINTI: "Düzeltilme önceliği"

Bu yüzden "raporda bir alan boş" tespitini doğru yapmışsın. Ancak öncelik alanı, hatanın NE ZAMAN/ HANGİ SIRAYLA düzeltileceğine dair yönetim/planlama bilgisidir; hatanın teknik olarak nasıl yeniden üretileceğine hiçbir katkısı yoktur. Soru "eksik alan hangisi?" değil, "yeniden üretmeye ne yardım eder?" diye sormaktadır.

(c şıkkı — her adımdan sonra bellek dökümü ve veritabanı anlık görüntüsü — orantısız ve raporu kullanılamaz hale getiren aşırı ek yüktür; d şıkkı ise aynı hatanın birden çok kopya raporunu üretir, bu da hata yönetimi iş akışına aykırıdır.)

**Ayırt edici fark:** Öncelik hatanın DÜZELTME SIRASINI belirler; etkilenen kullanıcı/kitap bilgisi ise hatanın YENİDEN ÜRETİLMESİ için gereken test verisidir.

**Yanılgı etiketi:** `hata-raporu-kritik-alan-onceliklendirme`

---

## Tekrar eden yanılgılar (özet)

| Etiket | Sorular | Ne anlama geliyor |
|---|---|---|
| `hata-raporu-vs-diger-surec-ciktisi-karisikligi` | C-37, D-36 | Hata raporuna ait içerik (durum, yeniden üretim adımları) ile yapılandırma yönetimi / test raporu içeriğinin sınırları karışıyor. Özellikle "DEĞİLDİR" tipi olumsuz sorularda hata yapılıyor. |
| `hata-raporu-kritik-alan-onceliklendirme` | C-38, D-38 | Hata raporu içerik listesi biliniyor ama "hangisi bu bağlamda EN kritik/EN yararlı" sıralaması yapılamıyor; meta veri alanları (ad, tarih, öncelik) ile yeniden üretim için gereken alanlar (ortam, sürüm, test verisi) eşit ağırlıkta görülüyor. |
| `konfigurasyon-yonetimi-izlenebilirlikle-karistirma` | A-37 | Sürüm/temel çizgi oluşturma (YY) ile iş ürünleri arasındaki bağ kurma (izlenebilirlik) ayrımı net değil. |
| `test-ilerleme-raporunun-tuketicisi-karisikligi` | C-36 | Test ilerleme raporunun hangi faaliyette girdi olarak kullanıldığı (testin tamamlanması) yerine planlama seçiliyor. |

## Çalışma önerisi
1. Bölüm 5.5'teki hata raporu içerik listesini (11 madde) ezberden yaz; her maddeyi "yeniden üretim için mi, yönetim/izleme için mi?" diye ikiye ayır. C-38 ve D-38 tam olarak bu ayrımı ölçüyor.
2. Bölüm 5.3.2'deki test ilerleme raporu (6 madde) ve test tamamlama raporu (7 madde) içeriklerini yan yana çalış; ikisi de "tekil hata ayrıntısı" içermez.
3. Bölüm 5.4'ün iki maddelik "YY şunları sağlar" listesini ezberle: (i) benzersiz tanımlama + versiyon kontrolü + değişiklik izleme + izlenebilirlik, (ii) tanımlı öğelerin test iş ürünlerinde açıkça belirtilmesi. Bu listede olmayan her şey (hata durumu, risk analizi vb.) YY değildir.

## Bölüm 6 — Test Araçları  (4 soru)

### A-39 · FL-6.1.1 · K2
**Senin cevabın:** d · **Doğru cevap:** c

**Neyi soruyor:** Test verisi hazırlama/oluşturma aracının, ISTQB test sürecindeki hangi aktivite grubuna hizmet ettiğini soruyor. Anahtar: test verisi "gereksinimi" tasarımda belirlenir ama test verisinin kendisi test uyarlamada üretilir ve koşumda kullanılır.

**Doğru şık neden doğru:** Test uyarlama (test implementation), test koşumu için gereken çalışma ürünlerini — test verisi dahil — oluşturma aktivitesidir; dolayısıyla test verisi hazırlama aracı "testin uyarlanması ve koşulması" aktivitesini destekler.
> ALINTI: "Test uyarlama test koşumu için gerekli test çalışma ürünlerini oluşturmayı veya edinmeyi içerir"

Test verisinin bir test uyarlama iş ürünü olduğu da açıkça sayılmıştır:
> ALINTI: "test grupları, test verisi, test koşumu çizelgesi ve test ortamı öğeleri."

Ayrıca araç kategorisi tarifi de bunu doğrular:
> ALINTI: "Test senaryoları, test verisi ve test prosedürlerini"

**Senin şıkkın neden yanlış:** d) "Test tamamlama", projenin/seviyenin bitişinde yapılan kapanış aktivitesidir; test verisi üretmez, aksine mevcut çalışma ürünlerini arşivler ve ortamı kapatır.
> ALINTI: "Gelecekte faydalı olabilecek test çalışma ürünleri belirlenir ve arşivlenir ya da uygun ekiplere"

**Ayırt edici fark:** Test uyarlama test verisini ÜRETİR (koşuma hazırlık), test tamamlama ise üretilmiş çalışma ürünlerini ARŞİVLER/KAPATIR.

**Yanılgı etiketi:** `test-uyarlama-yerine-test-tamamlama`

---
### B-39 · FL-6.1.1 · K2
**Senin cevabın:** b · **Doğru cevap:** c

**Neyi soruyor:** Dört araç tanımını (iş akışı takibi, iletişim, sanal makineler, gözden geçirme desteği) syllabus'taki dört araç kategorisiyle birebir eşleştirmeyi soruyor. Bu, 6.1'deki madde listesinin ezberden tanınmasını ölçen saf eşleştirme sorusudur.

**Doğru şık neden doğru:** c) 1C, 2D, 3B, 4A eşleşmesi syllabus'taki tanımların tam karşılığıdır:

1 → C (DevOps araçları), çünkü iş akışı takibi DevOps araçlarının tanımında geçer:
> ALINTI: "DevOps araçları: DevOps teslimat hattını, iş akışı takibini, otomatik derleme süreçlerini,"

2 → D (İş birliği araçları):
> ALINTI: "İş birliği araçları: İletişimi kolaylaştırır"

3 → B (Ölçeklenebilirlik/dağıtım standardizasyonu araçları), çünkü sanal makineler bu kategorinin örneğidir:
> ALINTI: "Ölçeklenebilirliği ve dağıtım standardizasyonunu destekleyen araçlar (ör. sanal"

4 → A (Statik test araçları), çünkü gözden geçirme desteği statik test araçlarının tanımıdır:
> ALINTI: "Statik test araçları: Gözden geçirmeler ve statik analiz konusunda test uzmanına destek sağlar"

**Senin şıkkın neden yanlış:** b) 1B, 2D, 3C, 4A dediğinde yalnızca 2 ve 4'ü doğru kurdun; 1 ve 3'ü yer değiştirdin. Yani "iş akışı takibi"ni ölçeklenebilirlik/dağıtım standardizasyonu araçlarına, "sanal makineler"i ise DevOps araçlarına bağladın. Sanal makineler DevOps teslimat hattında kullanılsa da syllabus onları açıkça ölçeklenebilirlik ve dağıtım standardizasyonu kategorisinin örneği olarak listeler; iş akışı takibi ise yalnızca DevOps araçları maddesinde geçer.

**Ayırt edici fark:** İş akışı takibi + CI/CD = DevOps araçları; sanal makine/konteynerleştirme = ölçeklenebilirliği ve dağıtım standardizasyonunu destekleyen araçlar.

**Yanılgı etiketi:** `devops-ile-sanallastirma-araci-karistirma`

---
### C-39 · FL-6.1.1 · K2
**Senin cevabın:** b · **Doğru cevap:** d

**Neyi soruyor:** Test senaryolarını, hataları ve yapılandırmayı bir arada "düzenleyen/yöneten" araç kategorisini soruyor. Üç farklı nesnenin (test + hata + yapılandırma) TEK bir araçta toplanması ipucudur.

**Doğru şık neden doğru:** Syllabus'ta yönetim araçları kategorisi tam olarak testleri, hataları ve yapılandırmayı birlikte kolaylaştıran kategoridir:
> ALINTI: "Yönetim araçları: YGYD yönetimini, gereksinimleri, testleri, hataları ve yapılandırmayı"
> ALINTI: "kolaylaştırarak test sürecinin verimliliğini artırır"

**Senin şıkkın neden yanlış:** b) "Test tasarımı ve uygulama araçları" yalnızca test çalışma ürünlerinin ÜRETİLMESİNİ kolaylaştırır; hata takibi ve yapılandırma yönetimi bu kategorinin tanımında yer almaz.
> ALINTI: "Test tasarımı ve test uygulama araçları: Test senaryoları, test verisi ve test prosedürlerini"
> ALINTI: "oluşturmayı kolaylaştırır"

Şıklardaki c) "Hata yönetimi araçları" da tuzaktır: yalnızca hataları kapsar, test senaryosu ve yapılandırmayı kapsamaz — soru üçünü birden istiyor.

**Ayırt edici fark:** Tasarım/uygulama araçları test çalışma ürünlerini OLUŞTURUR; yönetim araçları ise oluşturulmuş testleri, hataları ve yapılandırmayı ORGANİZE EDİP İZLER.

**Yanılgı etiketi:** `tasarim-araci-yerine-yonetim-araci`

---
### D-39 · FL-6.1.1 · K2
**Senin cevabın:** a · **Doğru cevap:** b

**Neyi soruyor:** Verilen beş araç kategorisinden hangilerinin doğrudan testlerin YÜRÜTÜLMESİNİ (koşulmasını) kolaylaştırdığını soruyor. Kategori listesi: i. İş birliği araçları, ii. DevOps araçları, iii. Yönetim araçları, iv. Fonksiyonel olmayan test araçları, v. Test tasarımı ve gerçekleştirme araçları.

**Doğru şık neden doğru:** b) ii, iv — DevOps araçları CI/CD ve otomatik derleme hattı üzerinden testlerin koşulmasını sağlar; fonksiyonel olmayan test araçları ise manuel olarak koşulması imkânsız testlerin fiilen yürütülmesine olanak verir.
> ALINTI: "DevOps araçları: DevOps teslimat hattını, iş akışı takibini, otomatik derleme süreçlerini,"
> ALINTI: "CI/CD'yi destekler"
> ALINTI: "Fonksiyonel olmayan test araçları: Test uzmanının manuel olarak yapılması zor veya imkansız"
> ALINTI: "olan fonksiyonel olmayan testleri yapmasına olanak sağlar"

Ayrıca CI/CD ve ilgili testlerin otomatik hatlarla koşulduğu da belirtilir:
> ALINTI: "Sürekli entegrasyon, sürekli teslimat, sürekli dağıtım ve ilgili testler genellikle otomatikleştirilmiş DevOps"

**Senin şıkkın neden yanlış:** a) i, v — "İş birliği araçları" iletişimi kolaylaştırır, test koşumuna doğrudan katkı vermez; "Test tasarımı ve gerçekleştirme araçları" ise test senaryosu, test verisi ve test prosedürlerini OLUŞTURUR, yani koşum ÖNCESİ hazırlık aktivitesini (test tasarımı/test uyarlama) destekler.
> ALINTI: "İş birliği araçları: İletişimi kolaylaştırır"
> ALINTI: "Test senaryoları, test verisi ve test prosedürlerini"

**Ayırt edici fark:** Tasarım/uygulama ve iş birliği araçları testleri koşuma HAZIRLAR; DevOps ve fonksiyonel olmayan test araçları testleri fiilen KOŞTURUR.

**Yanılgı etiketi:** `hazirlik-araci-ile-kosum-araci-karistirma`

---

## Bölüm 6 için özet ders

Dört sorunun dördü de aynı kökten: **araç kategorisi ↔ desteklediği test aktivitesi** eşleşmesi. 6.1'deki dokuz maddelik listeyi aktiviteye göre gruplayarak ezberle:

| Aktivite | Araç kategorisi |
|---|---|
| Planlama, gözetim, kontrol, hata/yapılandırma takibi | Yönetim araçları |
| Statik test (gözden geçirme + statik analiz) | Statik test araçları |
| Test analizi/tasarımı/uyarlaması (senaryo, veri, prosedür üretimi) | Test tasarımı ve test uygulama araçları |
| Test koşumu ve kapsam ölçümü | Test koşumu ve kapsam araçları |
| Fonksiyonel olmayan test koşumu | Fonksiyonel olmayan test araçları |
| İş akışı takibi, otomatik derleme, CI/CD | DevOps araçları |
| İletişim | İş birliği araçları |
| Sanal makineler, konteynerleştirme | Ölçeklenebilirliği ve dağıtım standardizasyonunu destekleyen araçlar |

---

# Ek — Tablo Tabanlı Sorular (koordinatlardan yeniden kurulmuş)

Aşağıdaki iki soru, PDF'ten düz metin çıkarımında tablo yapısı kaybolduğu için analiz
ajanları tarafından "sınırlı" olarak işaretlenmişti. Tablolar **koordinat tabanlı olarak
yeniden kurulmuş** ve çözümler bu gerçek veriden adım adım türetilmiştir. Her iki
sonuç da PDF'teki resmî cevap anahtarıyla bağımsız olarak örtüşmektedir.

### C-22 · FL-4.2.3 · K3 — Karar tablosunda çelişkili kural
**Senin cevabın:** `c` · **Doğru cevap:** `d`

Sorudaki karar tablosunun PDF'ten kurtarılan hâli:

| | R1 | R2 | R3 |
|:---|:---:|:---:|:---:|
| C1: Sınava ilk kez mi giriyorsunuz? | – | – | Y |
| C2: Teorik sınavı geçtiniz mi? | D | Y | – |
| C3: Pratik sınavı geçtiniz mi? | D | – | Y |
| **Ehliyet verilecek** | **X** | | |
| **Sınava tekrar başvuru yapıldı** | | **X** | |
| **Ek sürüş dersleri talep edildi** | | | **X** |

(D: Doğru, Y: Yanlış, –: önemsiz/don't care)

**Çelişkili kural ne demek:** Aynı girdi kombinasyonunun **birden fazla kurala** uyması ve bu
kuralların **farklı eylemler** üretmesidir. "–" işaretli koşullar o kuralda serbesttir, yani
kural o koşulun her değeriyle eşleşir — çelişki tam da buradan doğar.

**Adım adım kontrol:**

| Şık | Girdi | Eşleşen kurallar | Sonuç |
|:---|:---|:---|:---|
| a | C1=D, C2=D, C3=Y | R1 (C3=D ister) ✗ · R2 (C2=Y ister) ✗ · R3 (C1=Y ister) ✗ | Hiçbiri — bu bir **boşluk**, çelişki değil |
| b | C1=D, C2=Y, C3=D | R2 ✓ (C2=Y, diğerleri serbest) | Tek kural — çelişki yok |
| c | C1=D/Y, C2=D, C3=D | Yalnızca R1 ✓ | Tek kural — çelişki yok |
| **d** | **C1=Y, C2=Y, C3=Y** | **R2 ✓** (C2=Y, C1 ve C3 serbest) **ve R3 ✓** (C1=Y, C3=Y, C2 serbest) | **İki kural, iki farklı eylem → ÇELİŞKİ** |

**Senin şıkkın (c) neden yanlış:** İki ayrı girdi kombinasyonu vermişsin. Çelişki, iki farklı
girdinin yan yana konmasıyla değil, **tek bir girdinin iki kurala birden uymasıyla** oluşur.
Ayrıca verdiğin iki kombinasyon da yalnızca R1 ile eşleşiyor — ikisi de tek eylem üretiyor.

**Ayırt edici fark:** Çelişki = *bir girdi, birden çok kural, farklı eylemler.* Boşluk (gap) =
*bir girdi, hiçbir kural.* (a) şıkkı boşluğun örneğidir; (d) çelişkinin.

**Yanılgı etiketi:** `karar-tablosu-celiski-vs-bosluk`

---

### D-32 · FL-5.1.5 · K3 — Ek kapsama göre önceliklendirme
**Senin cevabın:** `d` · **Doğru cevap:** `b`

Sorudaki izlenebilirlik matrisinin PDF'ten kurtarılan hâli:

| | Ger1 | Ger2 | Ger3 | Ger4 | Ger5 | Ger6 | Ger7 |
|:---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **TS1** | X | | X | X | | | X |
| **TS2** | X | | | | | | X |
| **TS3** | | | | | X | X | |
| **TS4** | | X | | | | | |

**Ek kapsama önceliklendirmesi (additional coverage) nasıl işler:** Her adımda, o ana kadar
**henüz kapsanmamış** gereksinimden en çok sayıda karşılayan test senaryosu seçilir. Ölçüt
senaryonun toplam gereksinim sayısı değil, **yeni** kapsanan gereksinim sayısıdır.

**Adım adım türetme:**

| Sıra | Seçilen | Yeni kapsanan | Toplam kapsam |
|---:|:---|:---|:---|
| 1 | **TS1** | Ger1, Ger3, Ger4, Ger7 (**4 yeni**) | 4/7 |
| 2 | **TS3** | Ger5, Ger6 (**2 yeni**) | 6/7 |
| 3 | **TS4** | Ger2 (**1 yeni**) | 7/7 |
| 4 | **TS2** | Ger1 ve Ger7 — **ikisi de zaten kapsandı → 0 yeni** | 7/7 |

TS2 hiçbir yeni gereksinim eklemediği için **en sona** kalır → doğru cevap **b) TS2**.

**Senin şıkkın (d = TS4) neden yanlış:** TS4 matriste yalnızca **1** X işareti taşıdığı için "en
az kapsayan, o hâlde en sona" diye düşünülmüş olması muhtemeldir. Ancak TS4'ün kapsadığı Ger2'yi
**başka hiçbir senaryo kapsamıyor** — yani TS4 atlanırsa Ger2 hiç test edilmemiş kalır. TS4'ün
katkısı azdır ama **benzersizdir**; TS2'ninki ise sıfırdır.

**Ayırt edici fark:** Ek kapsama önceliklendirmesinde ölçüt **mutlak X sayısı** değil, sıraya
göre değişen **marjinal (yeni) katkıdır**. En sona kalan, en az X'i olan değil, katkısı sıfıra
düşen senaryodur.

**Yanılgı etiketi:** `mutlak-kapsam-vs-marjinal-kapsam-karisikligi`

---

# Ek — Karıştırılan Terimler Sözlüğü

Her terim için syllabus'tan BİREBİR alıntı verilmiştir. Alıntılar `raw/FoundationNotes.txt` (Türkçe FL v4.0 ders programı) içinde kelimesi kelimesine mevcuttur.

---

## 1) İnsan hatası (error) / Hata (defect) / Arıza (failure) / Kök neden (root cause)

**İnsan hatası — error / mistake**
> ALINTI: "İnsanlar  hata  (yanlışlık)  yapar  ve  bu  da  yazılım  hatalarına  (arıza,  hata)  neden  olur  ve  sonunda"
> ALINTI: "iletişim gibi birçok sebeple veya sadece yorgun oldukları ya da yeterli eğitime sahip olmadıkları için hata"

(Not: ilk alıntıdaki çift boşluklar PDF'in blok hizalamasından kaynaklanır, metinde aynen böyledir.)

**Hata — defect (koddaki/dokümandaki kusur)**
> ALINTI: "Hatalar, gereksinim veya test betiği gibi dokümantasyonda, kaynak kodda veya derleme dosyası gibi"
> ALINTI: "destekleyici bir eserde bulunabilir."

**Arıza — failure (çalışma anındaki dışa yansıyan yanlış davranış)**
> ALINTI: "Koddaki bir hata çalıştırılırsa sistem yapması gerekeni yapmayabilir veya yapmaması"
> ALINTI: "gereken bir şeyi yaparak bir arızaya neden olabilir."

Arızanın tek kaynağı hata değildir:
> ALINTI: "Arızaların tek sebebi insan hataları ve yazılım hataları değildir. Arızalar, radyasyon veya elektromanyetik"

**Kök neden — root cause**
> ALINTI: "Kök neden, bir problemin ortaya çıkmasının temel sebebidir (ör. hataya yol açan bir durum). Kök nedenler"
> ALINTI: "Kök nedenin ortadan kaldırılmasıyla benzer arızalar veya hatalar önlenebilir veya meydana"

**Ayrım (tek cümle):** İnsan hatası bir kişinin yaptığı yanlıştır, hata bu yanlışın iş ürününde bıraktığı statik kusurdur, arıza o hatanın çalıştırıldığında dışa yansıyan yanlış davranışıdır, kök neden ise zinciri başlatan temel sebeptir.

**Sınav ipucu:** Her hata arızaya yol açmaz —
> ALINTI: "arızaya neden olurken, bazıları belirli koşullar altında arızaya neden olur, bazıları ise hiçbir zaman"

---

## 2) Doğrulama (verification) / Geçerleme (validation)

> KAYNAK YOK: syllabus'ta doğrudan karşılık bulunamadı

(Türkçe FL v4.0 ders programı metninde "doğrulama/geçerleme" (verification/validation) çifti tanımlı bir terim çifti olarak geçmemektedir; bu nedenle alıntı verilmemiştir.)

---

## 3) Test gözetimi / test izleme (monitoring) / Test kontrolü (control)

**Test gözetimi**
> ALINTI: "Test gözetimi test hakkında bilgi toplamayla ilgilidir.  "
> ALINTI: "Test gözetimi tüm test aktivitelerinin devamlı izlenmesini ve planlanan"
> ALINTI: "ile gerçekleşenin karşılaştırılmasını içerir."

**Test kontrolü**
> ALINTI: "Test kontrolü, test hedeflerine ulaşmak için gerekli aksiyonları"
> ALINTI: "Test kontrolü, en etkili ve verimli testin gerçekleştirilmesi için kontrol yönergeleri şeklinde, rehberlik ve"
> ALINTI: "gerekli düzeltici aksiyonları sağlamak üzere test gözetiminden elde edilen bilgileri kullanır. Kontrol"

**Ayrım (tek cümle):** Gözetim BİLGİ TOPLAR (planlanan ile gerçekleşeni karşılaştırır), kontrol ise o bilgiyi kullanarak DÜZELTİCİ AKSİYON alır.

**Sınav ipucu:** "Testleri yeniden önceliklendirmek" bir kontrol aksiyonudur, gözetim değil —
> ALINTI: "Belirlenen bir risk sorun haline geldiğinde testleri yeniden önceliklendirmek"

---

## 4) Ürün riski / Proje riski

**Proje riski**
> ALINTI: "Proje riskleri projenin yönetimi ve kontrolüyle ilgilidir. Proje risklerine örnek olarak:"
> ALINTI: "Proje riskleri ortaya çıktığında, projenin zaman çizelgesini, bütçesini veya kapsamını etkileyebilir; bu da"

Proje riski örnekleri:
> ALINTI: "Teknik sorunlar (ör; proje kapsamının kontrolsüz artışı, eksik araç desteği)"
> ALINTI: "Tedarikçi sorunları (ör; tedarikçi teslimat başarısızlığı, tedarikçi iflası)"

**Ürün riski**
> ALINTI: "Ürün riskleri ürünün kalite karakteristikleriyle ilgilidir (ör. ISO 25010 kalite modelinde açıklanmıştır). Ürün"
> ALINTI: "riski örnekleri arasında şunlar yer alır: eksik ya da yanlış fonksiyonalite, hatalı hesaplamalar, çalışma"

**Ayrım (tek cümle):** Proje riski PROJENİN yürütülmesini (zaman, bütçe, kapsam, personel, tedarikçi) tehdit eder; ürün riski ise TESLİM EDİLEN ÜRÜNÜN kalite karakteristiklerini tehdit eder.

---

## 5) Giriş kriteri (entry criteria) / Çıkış kriteri (exit criteria)

> ALINTI: "Giriş kriterleri belirli bir aktivite için önkoşulları tanımlar. Giriş kriterleri karşılanmazsa faaliyetin daha zor"
> ALINTI: "Çıkış kriterleri bir aktivitenin"
> ALINTI: "tamamlandığını anlamak için nelere ulaşılması gerektiğini tanımlar."

Tipik örnekler:
> ALINTI: "Tipik giriş kriterleri arasında şunlar yer alır: kaynak elverişliliği (ör. insanlar, araçlar, ortamlar, test verisi,"
> ALINTI: "Tipik çıkış kriterleri arasında şunlar yer alır: bütünlük ölçüleri (ör. ulaşılan kapsam seviyesi, çözülmemiş"

Çevik karşılıkları:
> ALINTI: "Çevik yazılım geliştirmede, çıkış kriterleri genellikle Tamamlandı Tanımı olarak adlandırılır ve ekibin"
> ALINTI: "aktivitelerinin başlaması için yerine getirmesi gereken giriş kriterleri Hazır Tanımı olarak adlandırılır."

**Ayrım (tek cümle):** Giriş kriteri aktiviteye BAŞLAMAK için gereken önkoşulu, çıkış kriteri aktiviteyi BİTİRMİŞ saymak için gereken sonucu tanımlar.

**Sınav ipucu:** Zaman/para bitmesi geçerli bir ÇIKIŞ kriteridir —
> ALINTI: "Zamanın veya paranın bitmesi de geçerli bir çıkış kriteri olarak görülebilir. Diğer çıkış kriterleri yerine"

---

## 6) Test koşulu (test condition) / Test senaryosu (test case) / Test prosedürü (test procedure)

**Test koşulu — test analizi çıktısı ("ne test edilecek?")**
> ALINTI: "koşullarını tanımlamak ve önceliklendirmek üzere test esasının analiz edilmesini içerir (bkz. bölüm 5.2)."
> ALINTI: "Test analizi ölçülebilir kapsama kriterleri açısından "ne test edilecek?" sorusuna cevap verir."
> ALINTI: "Test analizi iş ürünleri şunları içerir: (önceliklendirilmiş) test koşulları (ör. kabul kriteri, bkz."

**Test senaryosu — test tasarımı çıktısı ("nasıl test edilecek?")**
> ALINTI: "Test tasarımı test koşullarının test senaryoları ve diğer test çalışma ürünleri olarak detaylandırılmasını"
> ALINTI: "Test tasarımı iş ürünleri şunları içerir: (önceliklendirilmiş) test senaryoları, test başlatma"

**Test prosedürü — test uyarlama çıktısı (koşum sırası/düzeni)**
> ALINTI: "Test senaryoları test prosedürleri şeklinde düzenlenebilir ve test grupları halinde birleştirilebilir."
> ALINTI: "Test prosedürleri, etkin test koşumu için test koşum çizelgesi"
> ALINTI: "Test uyarlama iş ürünleri şunları içerir: test prosedürleri, manuel ve otomatik test betikleri, "

**Ayrım (tek cümle):** Test koşulu NE test edileceğini söyler (analiz), test senaryosu bunu girdi/beklenen sonuç düzeyinde NASIL test edileceğine dönüştürür (tasarım), test prosedürü ise senaryoların HANGİ SIRAYLA koşulacağını düzenler (uyarlama).

---

## 7) Statik test / Dinamik test

> ALINTI: "Yazılım testleri dinamik veya statik olabilir. Dinamik test içerisinde yazılımın çalıştırılması yer alırken"
> ALINTI: "statik testte bu yoktur. Statik test, gözden geçirmeleri (bkz. konu 3) ve statik analizi içerir. Dinamik test,"
> ALINTI: "Dinamik testin aksine, statik testte test edilen yazılımın çalıştırılmasına gerek yoktur. Kod, süreç, sistem"

Farklar:
> ALINTI: "Dinamik testler, ilgili hataların daha sonra analiz yoluyla belirleneceği arızalara neden"
> ALINTI: "olurken, statik testler hataları doğrudan bulur."
> ALINTI: "Statik testler, kod üzerinde nadiren çalıştırılan veya dinamik testlerle zor ulaşılabilen yollar"

**Ayrım (tek cümle):** Dinamik test yazılımı ÇALIŞTIRIR ve arıza üzerinden hataya ulaşır; statik test yazılımı ÇALIŞTIRMADAN hatayı doğrudan bulur.

---

## 8) Gözden geçirme çeşitleri: Gayri resmi / Üzerinden geçme (izlekli prova) / Teknik gözden geçirme / Teftiş (denetim)

**Gayri resmi gözden geçirme**
> ALINTI: "Gayri resmi gözden geçirme. Gayri resmi gözden geçirmelerde tanımlanmış bir süreç"
> ALINTI: "izlenmez ve bunlar resmi olarak belgelenmiş bir çıktı gerektirmez. Ana hedef anomalileri"

**Üzerinden geçme (walkthrough / izlekli prova)**
> ALINTI: "Üzerinden geçme. Yazarın öncülüğündeki bir üzerinden geçme süreci kaliteyi değerlendirmek"
> ALINTI: "geçiriciler, üzerinden geçme süreci öncesinde bireysel gözden geçirme yapabilir ancak bu"
> ALINTI: "gerekli değildir."

**Teknik gözden geçirme**
> ALINTI: "Teknik Gözden Geçirme. Teknik gözden geçirmeler teknik açıdan nitelikli gözden geçiriciler"
> ALINTI: "tarafından gerçekleştirilir ve bir moderatör tarafından yönetilir. Teknik gözden geçirmenin"
> ALINTI: "amaçları arasında teknik bir problemle ilgili fikir birliği sağlamak ve buna ilişkin karar almak,"

**Teftiş (inspection / denetim)**
> ALINTI: "Teftiş. Teftişler en resmi gözden geçirme çeşidi olduğundan tanımlı gözden geçirme süreci"
> ALINTI: "eksiksiz olarak izlenir (bkz. bölüm 3.2.2). Ana hedef maksimum sayıda anomali bulmaktır. Diğer"
> ALINTI: "gözden geçirme lideri veya katip olarak görev yapamaz."

**Ayrım (tek cümle):** Resmiyet sırası gayri resmi < üzerinden geçme < teknik gözden geçirme < teftiş şeklinde artar; üzerinden geçmeyi YAZAR yönetir, teknik gözden geçirmeyi MODERATÖR yönetir ve teknik uzmanlar yapar, teftiş ise en resmi olanı olup metrik toplar ve yazarın lider/katip olmasını yasaklar.

**Hızlı ayırt tablosu**

| Çeşit | Kim yönetir | Resmiyet | Ana hedef |
|---|---|---|---|
| Gayri resmi | tanımlı süreç yok | en düşük | anomalileri tespit etmek |
| Üzerinden geçme | yazar | düşük–orta | kalite değerlendirme, fikir birliği, anomali tespiti |
| Teknik gözden geçirme | moderatör (teknik uzman gözden geçiriciler) | orta–yüksek | teknik fikir birliği ve karar |
| Teftiş | tanımlı sürecin tamamı; yazar lider/katip olamaz | en yüksek | maksimum sayıda anomali bulmak |

---

## 9) Test seviyesi (test level) / Test çeşidi (test type)

> ALINTI: "Test seviyeleri, birlikte düzenlenen ve yönetilen test aktivitesi gruplarıdır. Her test seviyesi, belirli bir"
> ALINTI: "yazılım geliştirme aşamasındaki yazılımla ilgili olarak gerçekleştirilen, bağımsız bileşenlerden komple"
> ALINTI: "Test çeşitleri belirli kalite karakteristikleriyle ilişkili test aktivitelerinin gruplarıdır ve bu test aktivitelerinin"
> ALINTI: "çoğu her test seviyesinde yapılabilir."

**Ayrım (tek cümle):** Test seviyesi testin NE ZAMAN / HANGİ ÖLÇEKTE (bileşen → sistem → kabul) yapıldığını belirtir; test çeşidi ise HANGİ KALİTE KARAKTERİSTİĞİNE odaklandığını belirtir ve her seviyede uygulanabilir.

**Sınav ipucu:** Dört test çeşidi her seviyede yapılabilir —
> ALINTI: "Yukarıda belirtilen dört test çeşidinin hepsi, her seviyede odak noktası farklı olsa da, tüm test"

---

## 10) Hata ayıklama (debugging) / Test etme (testing)

> ALINTI: "Test etme ve hata ayıklama birbirinden farklı aktivitelerdir. Test etme süreci yazılımdaki hataların neden"
> ALINTI: "olduğu arızaları tetikleyebilir (dinamik test) veya test nesnesindeki hataları doğrudan bulabilir (statik test)."
> ALINTI: "Dinamik test (bkz. konu 4) bir arızayı tetiklediğinde hata ayıklama işlemi bu arızanın (hataların)"
> ALINTI: "nedenlerinin bulunması, bu nedenlerin analiz edilmesi ve giderilmesiyle ilgilenir. Bu durumda tipik hata"

Hata ayıklama adımları:
> ALINTI: "Arızanın yeniden oluşturulması"
> ALINTI: "Teşhis (hatanın bulunması)"
> ALINTI: "Hatanın düzeltilmesi"

Statik testte hata ayıklama farklıdır:
> ALINTI: "Statik test bir hata bulduğunda hata ayıklama işlemi bu hatayı gidermekle ilgilenir. Statik test, hataları"
> ALINTI: "doğrudan bulduğundan ve arızalara neden olamayacağından yeniden oluşturmaya veya teşhise gerek"

**Ayrım (tek cümle):** Test etme arızayı/hatayı BULUR (test uzmanının işi), hata ayıklama ise bulunan arızanın nedenini teşhis edip DÜZELTİR (geliştiricinin işi).

**Sınav ipucu:** Düzeltmenin işe yaradığını onaylama testi kontrol eder —
> ALINTI: "Sonrasında gerçekleştirilen onaylama testleri düzeltmelerin problemi giderip gidermediğini kontrol eder."
> ALINTI: "Tercihen onaylama testi başlangıçtaki testi gerçekleştiren aynı kişi tarafından yapılır. Düzeltmelerin test"

---

## 11) EK — Test analizi / Test tasarımı / Test uyarlama / Test koşumu (sık karışan aktivite dörtlüsü)

> ALINTI: "Test analizi ölçülebilir kapsama kriterleri açısından "ne test edilecek?" sorusuna cevap verir."
> ALINTI: "Test uyarlama test koşumu için gerekli test çalışma ürünlerini oluşturmayı veya edinmeyi içerir"
> ALINTI: "Test koşumu testleri test koşum çizelgesine göre çalıştırmayı içerir. Test koşumu manuel veya otomatik"
> ALINTI: "olabilir."

**Ayrım (tek cümle):** Analiz test koşullarını çıkarır, tasarım test senaryolarını üretir, uyarlama koşum için gereken her şeyi (prosedür, betik, test verisi, ortam) hazırlar, koşum ise testleri çizelgeye göre çalıştırır.

---

## Doküman Doğrulama Kaydı

- Analiz edilen soru sayısı: **68** / 68
- Tüm syllabus alıntıları `FoundationNotes.pdf` metnine karşı birebir doğrulandı.
- Doğru cevaplar, FL kodları ve K seviyeleri sınav PDF'lerinin resmî cevap anahtarlarından
  otomatik çıkarıldı (dört sınav için de 40/40 satır eksiksiz).
- İşaretlenen ve doğru şıkların tamamı, ilgili sorunun gerçek seçenek satırlarıyla eşleştirildi.
