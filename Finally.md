# Finally — ISTQB Foundation Level (v4.0) Ezber Cümleleri

Örnek sınavlarda yanlış yapılan konulara ait **ISTQB FL v4.0 Türkçe syllabus**
cümleleri. Hepsi syllabus metninden **birebir** alınmış tam cümlelerdir —
hiçbiri yeniden yazılmamış, özetlenmemiş veya yorumlanmamıştır.

Toplam **207** cümle, 7 bölüm.

## İçindekiler

- [Karıştırılan Temel Terimler](#karıştırılan-temel-terimler) — 46 cümle
- [Bölüm 1 — Testin Temelleri](#bölüm-1--testin-temelleri) — 29 cümle
- [Bölüm 2 — Yazılım Geliştirme Yaşam Döngüsü Boyunca Test](#bölüm-2--yazılım-geliştirme-yaşam-döngüsü-boyunca-test) — 24 cümle
- [Bölüm 3 — Statik Test](#bölüm-3--statik-test) — 16 cümle
- [Bölüm 4 — Test Analizi ve Tasarımı](#bölüm-4--test-analizi-ve-tasarımı) — 46 cümle
- [Bölüm 5 — Test Faaliyetlerinin Yönetimi](#bölüm-5--test-faaliyetlerinin-yönetimi) — 39 cümle
- [Bölüm 6 — Test Araçları](#bölüm-6--test-araçları) — 7 cümle

---

## Karıştırılan Temel Terimler

### Hata (Error) · Hata (Defect) · Arıza (Failure) · Kök Neden

- İnsanlar hata (yanlışlık) yapar ve bu da yazılım hatalarına (arıza, hata) neden olur ve sonunda başarısızlık meydana gelir.
- İnsanlar zaman baskısı, iş ürünlerinin karmaşıklığı, süreçler, altyapı veya iletişim gibi birçok sebeple veya sadece yorgun oldukları ya da yeterli eğitime sahip olmadıkları için hata yapabilir.
- Hatalar, gereksinim veya test betiği gibi dokümantasyonda, kaynak kodda veya derleme dosyası gibi destekleyici bir eserde bulunabilir.
- Koddaki bir hata çalıştırılırsa sistem yapması gerekeni yapmayabilir veya yapmaması gereken bir şeyi yaparak bir arızaya neden olabilir.
- Arızaların tek sebebi insan hataları ve yazılım hataları değildir. Arızalar, radyasyon veya elektromanyetik alanın donanım yazılımında hatalara neden olması gibi çevresel koşullardan da kaynaklanabilir.
- Kök neden, bir problemin ortaya çıkmasının temel sebebidir (ör. hataya yol açan bir durum). Kök nedenler genellikle bir arıza olduğunda veya bir hata tespit edildiğinde gerçekleştirilen kök neden analiziyle belirlenir.
- Kök nedenin ortadan kaldırılmasıyla benzer arızalar veya hatalar önlenebilir veya meydana gelme sıklıkları azaltılabilir.

### Test Etme ve Hata Ayıklama (Debugging)

- Test etme ve hata ayıklama birbirinden farklı aktivitelerdir. Test etme süreci yazılımdaki hataların neden olduğu arızaları tetikleyebilir (dinamik test) veya test nesnesindeki hataları doğrudan bulabilir (statik test).
- Dinamik test (bkz. konu 4) bir arızayı tetiklediğinde hata ayıklama işlemi bu arızanın (hataların) nedenlerinin bulunması, bu nedenlerin analiz edilmesi ve giderilmesiyle ilgilenir. Bu durumda tipik hata ayıklama süreci şunları içerir:
- Arızanın yeniden oluşturulması
- Teşhis (hatanın bulunması)
- Hatanın düzeltilmesi Sonrasında gerçekleştirilen onaylama testleri düzeltmelerin problemi giderip gidermediğini kontrol eder.
- Statik test bir hata bulduğunda hata ayıklama işlemi bu hatayı gidermekle ilgilenir. Statik test, hataları doğrudan bulduğundan ve arızalara neden olamayacağından yeniden oluşturmaya veya teşhise gerek yoktur (bkz. konu 3).
- Tercihen onaylama testi başlangıçtaki testi gerçekleştiren aynı kişi tarafından yapılır. Düzeltmelerin test nesnesinin diğer bölümlerinde arızalara neden olup olmadığını kontrol etmek için daha sonra bir regresyon testi de yapılabilir (onaylama ve regresyon testine ilişkin daha detaylı bilgi için bkz. bölüm 2.2.3).

### Statik Test ve Dinamik Test

- Yazılım testleri dinamik veya statik olabilir. Dinamik test içerisinde yazılımın çalıştırılması yer alırken statik testte bu yoktur.
- Dinamik test içerisinde yazılımın çalıştırılması yer alırken statik testte bu yoktur. Statik test, gözden geçirmeleri (bkz. konu 3) ve statik analizi içerir. Dinamik test, farklı test teknikleri ve yaklaşımları kullanarak test senaryolarını elde eder (bkz. konu 4).
- Dinamik testin aksine, statik testte test edilen yazılımın çalıştırılmasına gerek yoktur. Kod, süreç, sistem mimarisi veya diğer iş ürünleri manuel incelemeyle (ör. gözden geçirme) veya bir araç yardımıyla (ör. statik analiz) değerlendirilir.
- Dinamik testler, ilgili hataların daha sonra analiz yoluyla belirleneceği arızalara neden olurken, statik testler hataları doğrudan bulur.
- Statik testler, kod üzerinde nadiren çalıştırılan veya dinamik testlerle zor ulaşılabilen yollar üzerindeki hataları daha kolay tespit edebilir.

### Test Seviyesi ve Test Çeşidi

- Test seviyeleri, birlikte düzenlenen ve yönetilen test aktivitesi gruplarıdır. Her test seviyesi, belirli bir yazılım geliştirme aşamasındaki yazılımla ilgili olarak gerçekleştirilen, bağımsız bileşenlerden komple sistemlere veya bazı durumlarda sistemlerin sistemlerine kadar gerçekleştirilen test sürecinin bir örneğidir.
- Test çeşitleri belirli kalite karakteristikleriyle ilişkili test aktivitelerinin gruplarıdır ve bu test aktivitelerinin çoğu her test seviyesinde yapılabilir.
- Yukarıda belirtilen dört test çeşidinin hepsi, her seviyede odak noktası farklı olsa da, tüm test seviyelerine uygulanabilir.

### Test Analizi · Test Tasarımı · Test Uyarlama · Test Koşumu

- Test analizi ölçülebilir kapsama kriterleri açısından "ne test edilecek?" sorusuna cevap verir.
- Test tasarımı iş ürünleri şunları içerir: (önceliklendirilmiş) test senaryoları, test başlatma belgeleri, kapsam öğeleri, test verisi gereksinimleri ve test ortamı gereksinimleri.
- Test uyarlama iş ürünleri şunları içerir: test prosedürleri, manuel ve otomatik test betikleri, test grupları, test verisi, test koşumu çizelgesi ve test ortamı öğeleri.
- Test koşumu testleri test koşum çizelgesine göre çalıştırmayı içerir. Test koşumu manuel veya otomatik olabilir.

### Test Gözetimi (İzleme) ve Test Kontrolü

- Test gözetimi test hakkında bilgi toplamayla ilgilidir.
- Test gözetimi tüm test aktivitelerinin devamlı izlenmesini ve planlanan ile gerçekleşenin karşılaştırılmasını içerir.
- Test kontrolü, test hedeflerine ulaşmak için gerekli aksiyonları almayı içerir.
- Test kontrolü, en etkili ve verimli testin gerçekleştirilmesi için kontrol yönergeleri şeklinde, rehberlik ve gerekli düzeltici aksiyonları sağlamak üzere test gözetiminden elde edilen bilgileri kullanır. Kontrol yönergelerine örnek olarak şunlar verilebilir:

### Ürün Riski ve Proje Riski

- Ürün riskleri ürünün kalite karakteristikleriyle ilgilidir (ör. ISO 25010 kalite modelinde açıklanmıştır). Ürün riski örnekleri arasında şunlar yer alır: eksik ya da yanlış fonksiyonalite, hatalı hesaplamalar, çalışma zamanı hataları, zayıf mimari, etkin olmayan algoritmalar, yetersiz yanıt süresi, kötü kullanıcı deneyimi, güvenlik açıkları.
- Proje riskleri projenin yönetimi ve kontrolüyle ilgilidir. Proje risklerine örnek olarak:
- Tedarikçi sorunları (ör; tedarikçi teslimat başarısızlığı, tedarikçi iflası) Proje riskleri ortaya çıktığında, projenin zaman çizelgesini, bütçesini veya kapsamını etkileyebilir; bu da projenin hedeflerine ulaşma kapasitesine etki eder.
- Teknik sorunlar (ör; proje kapsamının kontrolsüz artışı, eksik araç desteği)
- Belirlenen bir risk sorun haline geldiğinde testleri yeniden önceliklendirmek

### Giriş Kriteri ve Çıkış Kriteri

- Giriş kriterleri belirli bir aktivite için önkoşulları tanımlar. Giriş kriterleri karşılanmazsa faaliyetin daha zor olması, daha uzun sürmesi, daha maliyetli ve daha riskli olması muhtemeldir.
- Çıkış kriterleri bir aktivitenin tamamlandığını anlamak için nelere ulaşılması gerektiğini tanımlar.
- Çevik yazılım geliştirmede, çıkış kriterleri genellikle Tamamlandı Tanımı olarak adlandırılır ve ekibin piyasaya sürülebilir bir öğe için hedef metriklerini tanımlar.
- Bir kullanıcı hikayesinin geliştirme ve/veya test aktivitelerinin başlaması için yerine getirmesi gereken giriş kriterleri Hazır Tanımı olarak adlandırılır.
- Zamanın veya paranın bitmesi de geçerli bir çıkış kriteri olarak görülebilir. Diğer çıkış kriterleri yerine getirilmese bile paydaşlar daha fazla test yapmadan ürünü piyasaya sürmenin riskini gözden geçirip kabul ettiyse, bu şartlar altında testlere son verilmesi kabul edilebilir bir durumdur.

### Gözden Geçirme Çeşitleri

- Gayri resmi gözden geçirme. Gayri resmi gözden geçirmelerde tanımlanmış bir süreç izlenmez ve bunlar resmi olarak belgelenmiş bir çıktı gerektirmez.
- Gözden geçiriciler, üzerinden geçme süreci öncesinde bireysel gözden geçirme yapabilir ancak bu gerekli değildir.
- Teknik Gözden Geçirme. Teknik gözden geçirmeler teknik açıdan nitelikli gözden geçiriciler tarafından gerçekleştirilir ve bir moderatör tarafından yönetilir.
- Teknik gözden geçirmeler teknik açıdan nitelikli gözden geçiriciler tarafından gerçekleştirilir ve bir moderatör tarafından yönetilir. Teknik gözden geçirmenin amaçları arasında teknik bir problemle ilgili fikir birliği sağlamak ve buna ilişkin karar almak, anomalileri tespit etmek, kaliteyi değerlendirmek ve çalışma ürününe yönelik güven oluşturmak, yeni fikirler üretmek, yazarları iyileştirmeler yapmaya teşvik etmek ve buna olanak sağlamak yer alır.
- Teftiş. Teftişler en resmi gözden geçirme çeşidi olduğundan tanımlı gözden geçirme süreci eksiksiz olarak izlenir (bkz. bölüm 3.2.2).
- Teftişler en resmi gözden geçirme çeşidi olduğundan tanımlı gözden geçirme süreci eksiksiz olarak izlenir (bkz. bölüm 3.2.2). Ana hedef maksimum sayıda anomali bulmaktır. Diğer hedefler arasında kaliteyi değerlendirmek, çalışma ürününe yönelik güven oluşturmak, yazarları iyileştirmeler yapmaya teşvik etmek ve bunları yapabilmelerini sağlamak bulunur.

---

## Bölüm 1 — Testin Temelleri

### Test Hedefleri

- Arızaları tetiklemek ve hataları bulmak
- Belirtilen gereksinimlerin yerine getirilip getirilmediğini doğrulamak

### Yanlışlık, Hata, Arıza ve Kök Neden

- Bazı hatalar sistem çalıştırıldığında her zaman arızaya neden olurken, bazıları belirli koşullar altında arızaya neden olur, bazıları ise hiçbir zaman arızaya neden olmayabilir.

### Test Prensipleri

- Testler, test nesnesinde hataların mevcut olduğunu gösterebilir ancak hiç hata kalmadığını ispatlayamaz (Buxton 1970).
- Yeni hata bulamıyoruz başarılı bir yazılım elde ettik yanılgısı.
- Belirlenen tüm gereksinimleri titizlikle test etmek ve bulunan tüm hataları çözmek, kullanıcıların ihtiyaçlarını ve beklentilerini karşılamayan, müşterinin iş hedeflerine ulaşmasına yardımcı olmayan veya diğer rakip yazılımlara kıyasla daha zayıf bir yazılımın üretilmesini engelleyemeyebilir.
- Test sırasında doğrulamanın yanında sağlama da yapılmalıdır (Boehm 1981).

### Test Planlama, Gözetimi ve Kontrolü

- Test planlama test hedefini belirleyip ardından genel bağlam dahilinde gerekli olan kısıtlar kapsamında hedeflere en iyi şekilde ulaşılmasını sağlayacak yaklaşımı seçmektir.

### Test Analizi

- Test analizi test edilebilir özellikleri belirlemek ve ilgili riskler ve risk seviyeleri ile birlikte ilişkili test koşullarını tanımlamak ve önceliklendirmek üzere test esasının analiz edilmesini içerir (bkz. bölüm 5.2).
- Test esası ve test hedefleri aynı zamanda içerebilecekleri hataları belirlemek ve test edilebilirliği analiz etmek için de değerlendirilir.
- Test analizi genellikle test tekniklerinin kullanımıyla desteklenir (bkz. konu 4).

### Test Tasarımı

- Test tasarımı test koşullarının test senaryoları ve diğer test çalışma ürünleri olarak detaylandırılmasını içerir (ör. test başlatma belgeleri).
- Bu aktivite genellikle test senaryosu girdilerini belirlemeye yönelik bir rehber işlevi gören kapsam öğelerinin belirlenmesini içerir. Test teknikleri (bkz. konu 4) bu aktiviteyi desteklemek için kullanılabilir.

### Test Uyarlama

- Test uyarlama test koşumu için gerekli test çalışma ürünlerini oluşturmayı veya edinmeyi içerir (bkz. test verisi).
- Test senaryoları test prosedürleri şeklinde düzenlenebilir ve test grupları halinde birleştirilebilir.
- Test ortamı oluşturulur ve kurulumunun uygun bir şekilde yapıldığı doğrulanır.

### Test Koşumu

- Gerçek test sonuçları beklenen sonuçlarla karşılaştırılır. Test sonuçları kaydedilir. Olası nedenlerin belirlenmesi için anomaliler analiz edilir.

### Test Tamamlama

- Gelecekte faydalı olabilecek test çalışma ürünleri belirlenir ve arşivlenir ya da uygun ekiplere devredilir.
- Test tamamlama raporu oluşturulur ve paydaşlara iletilir.

### Test Çalışma Ürünleri

- Test gözetimi ve test kontrolü iş ürünleri şunları içerir: test ilerleme raporları (bkz. bölüm 5.3.2), kontrol direktifleri dokümantasyonu (bkz. bölüm 5.3) ve risk bilgisi (bkz. bölüm 5.2). • Test analizi iş ürünleri şunları içerir: (önceliklendirilmiş) test koşulları (ör. kabul kriteri, bkz. bölüm 4.5.2) ve test esasındaki hatalara ilişkin hata raporu.
- Test prosedürleri, etkin test koşumu için test koşum çizelgesi kapsamında önceliklendirilip düzenlenir (bkz. bölüm 5.1.5).
- Test tamamlama iş ürünleri şunları içerir: test tamamlama raporu (bkz. bölüm 5.3.2), sonraki proje veya döngülerin iyileştirilmesine yönelik aksiyon öğeleri, tecrübeler ve değişiklik talepleri (ör. ürün iş listesi öğeleri).

### Test Rolleri

- Test etme rolü testin mühendislik (teknik) yönünün tüm sorumluluğuna sahiptir. Test etme rolü temelde test analizi, test tasarımı, test uyarlama ve test koşumu aktivitelerine odaklanır.
- Test yönetimi rolü, genel olarak test sürecinden, test ekibinden ve test aktivitelerine liderlik edilmesinden sorumludur. Test yönetimi rolü temelde test planlama, test gözetimi ve kontrolü ve test tamamlama aktivitelerine odaklıdır.
- Örneğin, Çevik Yazılım Geliştirmede bazı test yönetimi görevleri Çevik ekip tarafından gerçekleştirilirken, birden fazla ekibi veya tüm organizasyonu ilgilendiren görevler geliştirme ekipleri dışındaki test yöneticileri tarafından yerine getirilebilir.

### Tüm Ekip Yaklaşımı

- Tüm ekip yaklaşımında, gerekli bilgi ve beceriye sahip tüm ekip üyeleri her türlü görevi yapabilir ve kaliteden herkes sorumludur.
- Tüm ekip yaklaşımı ekip ilişkilerini geliştirir, ekip içinde iletişimi ve iş birliğini artırır ve ekibin farklı beceri setlerinin proje yararına kullanılmasına olanak sağlayarak sinerji yaratır.
- Ekip üyeleri aynı çalışma alanını (fiziksel veya sanal) paylaşır çünkü ortak çalışma alanı iletişim ve etkileşimi kolaylaştırır.
- Bu, uygun kabul testleri oluşturmalarına yardımcı olmak için iş birimleriyle iş birliği yapmanın yanı sıra test stratejisi ve test otomasyonu metodolojilerine karar vermek için yazılımcılarla birlikte çalışmayı da içerir.

---

## Bölüm 2 — Yazılım Geliştirme Yaşam Döngüsü Boyunca Test

### Yazılım Geliştirme Yaşam Döngüsü ve Test — İyi Test Uygulamaları

- Her yazılım geliştirme faaliyetine karşılık gelen bir test faaliyeti vardır ve böylece tüm geliştirme faaliyetlerinin kalite kontrole tabi olması sağlanır.
- Farklı test seviyeleri (bkz. konu 2.2.1) belirli ve farklı test hedeflerine sahiptir ve bu da testin uygun şekilde kapsamlı olmasına olanak tanırken gereksiz tekrarlardan kaçınmayı sağlar.
- Belirli bir test seviyesi için test analizi ve tasarımı YGYD'nin ilgili geliştirme aşamasında başlar ve böylece test "erken test" prensibine uygun şekilde test gerçekleşebilir.
- Test uzmanları, iş ürünlerinin taslakları hazır olur olmaz iş ürünlerini gözden geçirme sürecine dahil olur, böylece erken test ve hata tespiti "shift-left" yaklaşımını destekleyebilir (bkz. bölüm 2.1.5).

### Yazılım Geliştirme Modelleri ve Test

- Test uzmanının rol ve sorumlulukları Sıralı yazılım geliştirme modellerinde, ilk aşamalarda test uzmanları genellikle gereksinim gözden geçirmelerine, test analizine ve test tasarımına katılır.
- Çalıştırılabilir kod genellikle sonraki aşamalarda oluşturulur, bu nedenle tipik olarak dinamik testler YGYD'nin erken aşamalarında gerçekleştirilemez.
- Bileşen testi normalde geliştiriciler tarafından kendi geliştirme ortamlarında yapılır.
- Yazılım özelliklerinin sık hayata geçirilmesi hızlı geri bildirim ve kapsamlı regresyon testleri gerektirir.
- Bu nedenle, çevik projelerde iş ürünü belgelerinin hafifletilmesi ve regresyon testlerini kolaylaştırmak için kapsamlı test otomasyonu tercih edilir.

### Test Öncelikli Yaklaşımlar

- Bu yaklaşımların her biri erken test etme prensibini uygular (bkz. bölüm 1.3) ve shift-left yaklaşımını izler (bkz. bölüm 2.1.5), çünkü testler kod yazılmadan önce tanımlanır.
- Davranış Güdümlü Yazılım Geliştirme (BDD): - Uygulamanın istenen davranışını, genellikle Given/When/Then formatı kullanılarak, paydaşlar tarafından anlaşılması kolay bir doğal dilin basit bir formunda yazılan test senaryoları ile ifade eder.

### Shift-Left Yaklaşımı

- Shift-left genellikle testlerin daha erken yapılmasını önerir (örneğin, kodun yazılmasını veya bileşenlerin entegre edilmesini beklemeden), ancak bu YGYD'nin ilerleyen aşamalarında testlerin ihmal edilmesi gerektiği anlamına gelmez.
- Testçilerin bakış açısıyla analizin gözden geçirilmesi.
- Kod yazılmadan önce test senaryolarının yazılması ve kodun yazılması sırasında kodun bir test kuluçkasında çalıştırılması
- Bu bir tür shift-left uygulamasıdır.

### DevOps ve Test

- DevOps teslimat hattı tanımlanmalı ve kurulmalıdır
- Stabil test ortamları oluşturmayı kolaylaştıran CI/CD gibi otomatik süreçleri destekler
- Test otomasyonu ek kaynaklar gerektirir. Test otomasyonunun kurması ve sürdürmesi zor olabilir Her ne kadar DevOps kapsamında yüksek düzeyde test otomasyonu bulunsa da özellikle kullanıcı perspektifinden bakıldığında manuel testlere yine de ihtiyaç olacaktır.
- Fonksiyonel olmayan kalite karakteristiklerine (ör. performans verimliliği ve güvenilirlik) ilişkin görünürlüğü artırır.

### Test Seviyeleri

- Bileşen entegrasyon testi (birim entegrasyon testi olarak da bilinir) arayüzlerin ve bileşenler arasındaki etkileşimlerin testine odaklanır.
- Sistem entegrasyon testi test edilen sistem ile diğer sistemler ve harici hizmetler arasındaki arayüzlerin test edilmesine odaklanır.
- Sistem testi bir sistemin veya ürünün genel davranışına ve yeteneklerine odaklanır, genellikle uçtan uca görevlerin fonksiyonel testlerini ve kalite karakteristiklerine ilişkin fonksiyonel olmayan testleri içerir.
- Sistem testi bağımsız bir test ekibi tarafından yapılabilir ve sisteme yönelik gereksinimlerle ilgilidir.
- Başlıca kabul testi çeşitleri şunlardır: kullanıcı kabul testi (KKT), operasyonel kabul testi, sözleşmesel kabul testi ve düzenleyici kabul testi, alfa testi ve beta testi.

---

## Bölüm 3 — Statik Test

### Statik Testin Faydaları

- Statik test YGYD'nin erken aşamalarında hataları tespit ederek erken test prensibini yerine getirebilir (bkz. bölüm 1.3).
- Çünkü projenin ilerleyen aşamalarında hataları düzeltmek için daha fazla zaman ve efor harcanması gerekir.

### Statik Test ile Dinamik Testin Farkı

- Ayrıca, dinamik testle tespit edilemeyecek hataları da bulabilir (ör. ulaşılamayan kod, istenildiği gibi uygulanmayan tasarım örüntüleri, çalıştırılamayan iş ürünlerindeki hatalar).
- Statik ve dinamik testlerin (arıza analiziyle) her ikisi de hataların tespit edilmesini sağlayabilir ancak bazı hata çeşitleri ya statik testle ya da dinamik testle bulunabilir.

### Paydaş Geri Bildirimi

- YGYD boyunca sıkça verilen paydaş geri bildirimleri gereksinimler hakkındaki yanlış anlaşılmaları önleyebilir ve gereksinimlerdeki değişikliklerin daha erken anlaşılmasını ve uygulanmasını sağlayabilir.
- Paydaşlara en çok değer katacak ve belirlenen riskler üzerinde en olumlu katkıyı yapacak özelliklere odaklanmalarını sağlar.

### Gözden Geçirme Süreci

- Planlama aşamasında amaç, gözden geçirilecek çalışma ürünü, değerlendirilecek kalite karakteristiği, odaklanılacak alanlar, çıkış kriterleri, standartlar, efor gibi destekleyici bilgiler ve gözden geçirmeye ilişkin zaman dilimlerini içeren gözden geçirme kapsamı tanımlanır.
- Bu, her katılımcının gözden geçirilen çalışma ürününe erişebilmesini, rollerini ve sorumluluklarını anlamasını ve gözden geçirmenin yapılması için gereken her şeyin karşılanmasını da içerir.
- Her gözden geçirici, gözden geçirilen çalışma ürününün kalitesini değerlendirmek ve bir veya daha fazla gözden geçirme tekniğini uygulayarak (ör. kontrol listesine dayalı gözden geçirme, senaryoya dayalı gözden geçirme) anomalileri, önerileri ve soruları belirlemek için bireysel bir gözden geçirme yapar.
- Gözden geçirme sırasında tespit edilen anomalilerin hata olması gerekmediğinden, tüm bu anomalilerin analiz edilmesi ve tartışılması gerekir.

### Gayri Resmi Gözden Geçirme

- Gayri resmi gözden geçirmelerde tanımlanmış bir süreç izlenmez ve bunlar resmi olarak belgelenmiş bir çıktı gerektirmez. Ana hedef anomalileri tespit etmektir.

### Üzerinden Geçme

- Üzerinden geçme. Yazarın öncülüğündeki bir üzerinden geçme süreci kaliteyi değerlendirmek ve çalışma ürününe yönelik güven oluşturmak, gözden geçiricileri eğitmek, fikir birliğine varmak, yeni fikirler üretmek, yazarları durumları iyileştirmeye ve anomalileri tespit etmeye teşvik etmek ve bunu yapabilmelerini sağlamak gibi birçok amaca hizmet edebilir.

### Teftiş

- Metrikler toplanır ve teftiş süreci de dahil olmak üzere YGYD'nü iyileştirmek için kullanılır.
- Teftişte yazar; gözden geçirme lideri veya katip olarak görev yapamaz.

### Gözden Geçirmelerde Başarı Faktörleri

- Gözden geçirmeye hazırlanmaları için katılımcılara yeterli sürenin verilmesi
- Gözden geçiriciler bireysel gözden geçirme ve/veya (yapılıyorsa) gözden geçirme toplantısı sırasında konsantrasyonlarını kaybetmesinler diye gözden geçirmelerin küçük parçalar üzerinde gerçekleştirilmesi

---

## Bölüm 4 — Test Analizi ve Tasarımı

### Kara Kutu ve Beyaz Kutu Test Tekniklerinin Ayrımı

- Kara kutu test teknikleri (spesifikasyon bazlı teknikler olarak da bilinir) test nesnesinin iç yapısına atıfta bulunulmadan test nesnesinin davranışının analiz edilmesine dayanır. Bu nedenle test senaryoları yazılımın nasıl yazıldığından bağımsızdır.
- Bu nedenle test senaryoları yazılımın nasıl yazıldığından bağımsızdır. Sonuç olarak, kod değişir ancak test nesnesinin davranışı aynı kalırsa test senaryoları da hâlâ faydalı demektir.
- Beyaz kutu test teknikleri (yapı bazlı teknik olarak da bilinir) test nesnesinin iç yapısının ve işlemlerinin analizine dayanır. Test senaryoları yazılımın nasıl tasarlandığına bağlı olduğundan sadece test nesnesinin tasarımı veya kodlanmasından sonra oluşturulabilir.

### Denklik Paylarına Ayırma (DPA)

- DPA'da kapsam öğeleri denklik paylarıdır. Bu teknikle kapsamın %100'üne ulaşmak için test senaryoları, her payı en az bir kez kapsama alarak, belirlenmiş tüm payları (geçersiz paylar dahil) denemesi gerekmektedir.
- Tüm geçişler kapsamının %100'üne ulaşmak için test senaryoları tüm geçerli geçişleri denemeli ve geçersiz geçişleri denemeye çalışmalıdır. Tek bir test senaryosunda yalnızca bir geçersiz geçişin test edilmesi, kusur maskelenmesini, yani bir hatanın diğerinin tespitini engellediği durumları önlemeye yardımcı olur.
- Kapsam, denenen payların sayısının, tanımlanan payların toplam sayısına bölünmesiyle ölçülür ve yüzde olarak ifade edilir.
- Each Choice kapsamı, test senaryolarının her pay grubundan her bir payı en az bir kez denemesini gerektirir. Each Choice kapsamı pay kombinasyonlarını dikkate almaz.
- Dolayısıyla her pay için bir test yapılması yeterlidir.

### Sınır Değer Analizi (SDA)

- Dolayısıyla SDA sadece sıralı verilerden oluşan paylarda kullanılabilir. Bir payın minimum ve maksimum değerleri o payın sınır değerleridir.
- Bunlar: sınır değer ve bitişik paya ait en yakın komşusu. 2 değerli SDA ile %100 kapsama ulaşmak için test senaryolarının tüm kapsam öğelerini, yani tanımlanan tüm sınır değerlerini denemesi gerekir.
- 3 değerli SDA'da (Koomen 2006, O'Regan 2019) her sınır değer için üç kapsam öğesi vardır. Bunlar: sınır değer ve bu sınır değerin her iki komşu sınır değeri.
- Bunlar: sınır değer ve bu sınır değerin her iki komşu sınır değeri. Dolayısıyla 3 değerli SDA'da bazı kapsam öğeleri sınır değerler olmayabilir.
- Dolayısıyla 3 değerli SDA'da bazı kapsam öğeleri sınır değerler olmayabilir. 3 değerli SDA ile %100 kapsama ulaşmak için test senaryolarının tüm kapsam öğelerini, yani tanımlanan sınır değerleri ve komşu değerlerini denemesi gerekir.
- Kapsam, test senaryolarında denenen sınır değerlerin sayısının tanımlanan tüm sınır değerlerin sayısına bölünmesiyle ölçülür ve yüzde olarak ifade edilir.

### Karar Tablosu Testi

- Bunlar tablonun satırlarını oluşturur. Her sütun, koşulların benzersiz bir kombinasyonunu ve ilişkili aksiyonları tanımlayan bir karar kuralına karşılık gelir.
- "-", koşulun değerinin aksiyon çıktısı açısından ilgisiz olduğu anlamına gelir.
- Karar tablosu testlerinin güçlü yanı, hiçbir koşulu göz ardı etmeden tüm koşul kombinasyonlarını ele almaya yönelik sistematik bir yaklaşım sağlamasıdır. Ayrıca gereksinimlerdeki boşlukları veya çelişkileri bulmaya da yardımcı olur.

### Durum Geçiş Testi

- Durum geçişi diyagramına veya durum tablosuna dayalı bir test senaryosu genelde, bir dizi durum değişikliğiyle (ve gerekirse aksiyonla) sonuçlanan bir dizi olayla temsil edilir. Bir test senaryosu, durumlar arası çeşitli geçişleri içerebilir.
- Geçerli geçişler kapsamında (0-anahtar kapsamı da denir) kapsam öğeleri tekil geçerli geçişlerdir.
- Geçerli geçişler kapsamının %100'üne ulaşmak için test senaryoları tüm geçerli geçişleri denemelidir.

### Komut (İfade) Testi ve Dal Testi

- Komut testinde kapsam öğeleri çalıştırılabilir komutlardır.
- Dal, test nesnesinde komutların çalıştırıldığı olası sıraları gösteren kontrol akış grafiğindeki iki düğüm arasında gerçekleşen bir kontrol transferidir.
- Her bir kontrol transferi koşulsuz (ör. doğrudan açık kod) veya koşullu (ör. karar çıktısı) olabilir.
- Dal testlerinde kapsam öğeleri dallardır ve burada amaç, kabul edilebilir bir kapsama seviyesi elde edilene kadar kod içindeki dalları deneyecek test senaryoları tasarlamaktır.
- Kapsam, test senaryoları tarafından denenen dal sayısının toplam dal sayısına bölünmesiyle ölçülür ve yüzde olarak ifade edilir. %100 dal kapsamına ulaşıldığında, kod içindeki koşulsuz ve koşullu tüm dallar test senaryoları tarafından denenir.

### Beyaz Kutu Testinin Değeri

- Sadece kara kutu testi gerçekleştirmek, gerçek kod kapsamının ölçülmesini sağlamaz.
- Beyaz kutu kapsam ölçüleri objektif bir kapsam ölçümü sağlar ve bu kapsamı büyütmek için üretilecek ek testlere olanak sağlayan gerekli bilgileri sunar ve dolayısıyla koda yönelik güveni artırır.

### Hata Tahminleme

- Hata tahminleme, test uzmanının bilgilerine dayalı olarak insan hatalarının, yazılım hatalarının ve arızaların ortaya çıkmasını sağlamak için kullanılan bir tekniktir; bu bilgiler aşağıdaki gibidir:
- Diğer benzer uygulamalarda oluşan arıza çeşitleri Genel olarak insan hataları, yazılım hataları ve arızalar şunlarla ilgili olabilir: girdi (ör. doğru girdinin kabul edilmemesi, yanlış veya eksik parametreler), çıktı (ör. yanlış format, yanlış sonuç), mantık (ör. eksik senaryolar, yanlış operatör), hesaplama (ör. yanlış işlenen, yanlış hesaplama), arayüz (ör. parametre uyuşmazlığı, uyumsuz türler) veya veriler (ör. yanlış öndeğer atama, yanlış tür).
- Bu teknikte test uzmanının olası insan hatalarının, yazılım hatalarının ve arızaların bir listesini oluşturması veya elde etmesi ve insan hatalarıyla ilişkili hataları tanımlayacak, hataları ortaya çıkaracak veya arızalara neden olacak testler tasarlaması gerekir.
- Kusur ortaya çıkarmaya yönelik saldırılar hata tahminlemenin uygulanmasına yönelik metodik bir yaklaşımdır.

### Keşif Testi

- Keşif testinde, test uzmanı test nesnesi hakkında bilgi edinirken testler eş zamanlı olarak tasarlanır, koşulur ve değerlendirilir.
- Kapsam öğeleri test oturumunda tanımlanır ve denenir.
- Test uzmanı deneyimli, alan bilgisine sahip ve analitik beceriler, merak ve yaratıcılık gibi üst seviye temel becerilere sahipse keşif testleri daha etkili olacaktır (bkz. bölüm 1.5.1).
- Keşif testleri, gereksinimler az veya yetersiz olduğunda veya testler üzerinde önemli bir zaman baskısı olduğunda işe yarar.

### Kontrol Listesi Bazlı Test

- Ayrıntılı test senaryolarının olmadığı durumlarda, kontrol listesine dayalı testler, test süreci için yol gösterici olabilir.
- Kontrol listesi öğeleri genellikle soru şeklindedir. Her öğe ayrı ayrı ve doğrudan kontrol edilebilir olmalıdır.
- Bu öğeler gereksinimlere, arayüz özelliklerine, kalite karakteristiğine veya diğer test koşulu biçimlerine ilişkin olabilir.
- Kontrol listeleri otomatik olarak kontrol edilebilecek öğeleri, daha çok giriş/çıkış kriteri olmaya uygun olan öğeleri veya çok genel olan öğeleri içermez (Brykczynski 1999).
- Bu kontrol listeleri üst seviye listeler olduğu için, gerçek testlerde bazı değişikliklerin ortaya çıkması muhtemeldir; bu da potansiyel olarak daha büyük kapsama ama daha düşük tekrarlanabilirliğe yol açar.

### Kullanıcı Hikâyeleri ve 3C

- Conversation (Konuşmalar): Yazılımın nasıl kullanılacağını açıklar (belgeyle veya sözlü olabilir)
- Kabul kriterleri genelde bir konuşma sonunda ortaya çıkar (bkz. bölüm 4.5.1).
- İş birliği, ekibin analiz, yazılım geliştirme ve test etme gibi üç perspektifi dikkate alarak, neyin teslim edilmesi gerektiğine yönelik ortak bir vizyon edinmesini sağlar.

### Kabul Kriterleri

- Bir kullanıcı hikayesi için kabul kriterleri, bu kullanıcı hikayesinin, paydaşlar tarafından kabul edilmesi için karşılaması gereken koşulları içerir.
- Senaryo odaklı (ör. BDD'de kullanılan Given/When/Then formatı, bkz. bölüm 2.1.3)
- Kural odaklı (ör. madde işaretli kontrol listesi veya girdi-çıktı eşlemesinin tablo haline getirilmiş şekli) Çoğu kabul kriteri bu iki formattan birinde dokümante edilebilir.

---

## Bölüm 5 — Test Faaliyetlerinin Yönetimi

### Test Planlaması ve Test Uzmanının Rolü

- Sürüm planlamasında yer alan test uzmanları, test edilebilir kullanıcı hikayelerinin ve kabul kriterlerinin yazım sürecine katılır (bkz. bölüm 4.5), proje ve kalite riski analizlerinde görev alır (bkz. bölüm 5.2), kullanıcı hikayeleriyle ilişkili test eforunu tahmin eder (bkz. bölüm 5.1.4), test yaklaşımını belirler ve sürüm için testi planlar.
- Döngü planlamasında yer alan test uzmanları, kullanıcı hikayelerine ilişkin detaylı bir risk analizine katılır, kullanıcı hikayelerinin test edilebilirliğini belirler, kullanıcı hikayelerini görevlere (özellikle test görevleri) ayırır, tüm test görevleri için test eforuna dair tahminde bulunur ve fonksiyonel ve fonksiyonel olmayan test nesnesi unsurlarını belirler ve iyileştirir.

### Giriş ve Çıkış Kriterleri

- Tipik giriş kriterleri arasında şunlar yer alır: kaynak elverişliliği (ör. insanlar, araçlar, ortamlar, test verisi, bütçe, zaman), test çalışma ürünleri elverişliliği (ör. test esası, test edilebilir gereksinimler, kullanıcı hikayeleri, test senaryoları) ve test nesnesinin başlangıç kalite seviyesi (ör. tüm duman testleri geçmiştir).
- Tipik çıkış kriterleri arasında şunlar yer alır: bütünlük ölçüleri (ör. ulaşılan kapsam seviyesi, çözülmemiş hata sayısı, hata yoğunluğu, başarısız test senaryosu sayısı) ve ikili "evet/hayır" kriterleri (ör. planlanan testler koşturuldu, statik test yapıldı, bulunan tüm hatalar raporlandı, tüm regresyon testleri otomatik hale getirildi).

### Test Tahmin Teknikleri

- Bu metrik bazlı teknikte, kuruluş içinde önceden yapılmış projelerden edinilen rakamlar toplanır ve bu da benzer projeler için "standart" oranların elde edilmesini mümkün kılar.
- Örneğin, bir önceki projede "geliştirme-test" eforu oranı 3:2 ise ve mevcut projede geliştirme eforunun 600 kişi-gün olması bekleniyorsa test eforunun 400 kişi-gün olacağı tahmin edilebilir.

### Test Senaryolarının Önceliklendirilmesi

- İdeal olarak test senaryoları, yukarıdaki önceliklendirme stratejilerinden biri kullanılarak öncelik seviyelerine göre çalıştırılacak şekilde sıralanır.
- Yüksek öncelikli bir test senaryosu düşük öncelikli bir test senaryosuna bağımlıysa önce düşük öncelikli test senaryosu koşturulmalıdır.
- Ek kapsam önceliklendirmesi denilen başka bir varyantta, en yüksek kapsama ulaşan test senaryosu ilk uygulanır; sonraki her bir test senaryosu en yüksek ek kapsama ulaşan test senaryosudur.

### Test Piramidi

- Test piramidi, farklı testlerin farklı ayrıntıları olabileceğini gösteren bir modeldir.
- Katman ne kadar yüksekse test ayrıntısı, test izolasyonu o kadar düşük, test koşumu süresi ise o kadar yüksek olur.

### Test Çeyrekleri

- Brian Marick (Marick 2003, Crispin 2008) tarafından tanımlanan test çeyrekleri, test seviyelerini Çevik yazılım geliştirmede uygun test çeşitleri, aktiviteleri, test teknikleri ve iş ürünleri ile gruplandırır.
- Bu modelde testler iş odaklı veya teknoloji odaklı olabilir.
- Bu model ayrıca geliştiriciler, test uzmanları ve iş birimleri dahil tüm paydaşlara test çeşitlerinin ayrımını yapmanın ve açıklamanın bir yolunu sunar.
- Model, tüm uygun test çeşitlerinin ve test seviyelerinin YGYD'ne dahil edilmesini sağlamak için bunları görselleştirmede ve bazı test çeşitlerinin belirli test seviyeleriyle diğerlerinden daha alakalı olduğunu anlamada test yönetimini destekler.

### Risk Kavramı ve Risk Seviyesi

- Risk etkisi (zarar) - riskin meydana gelmesinin sonuçları Versiyon v4.0 Bu iki faktör bir risk ölçüsü olan risk seviyesini belirtir. Risk seviyesi ne kadar yüksekse çözülmesi de o kadar önemlidir.

### Ürün Riski Analizi ve Kullanımı

- Ürün riski analizi, testlerin bütünlüğünü ve kapsamını etkileyebilir. Sonuçları aşağıdaki amaçlarla kullanılır:
- Kullanılacak test tekniklerini ve ulaşılacak kapsamı belirlemek

### Risk Kontrolü ve Risk Azaltma

- Ürün risk kontrolüne ilişkin olarak bir risk analiz edildiğinde riske yönelik birkaç yanıt seçeneği mümkündür; örneğin, test yoluyla riskin azaltılması, risk kabulü, risk transferi veya acil durum planı (Veenendaal 2012).
- Uygun test teknikleri ve kapsam seviyeleri uygulamak
- Etkilenen kalite karakteristiklerini hedefleyen uygun test çeşitlerini uygulamak.

### Test İzleme, Kontrol ve Raporlama

- Test raporunda test öncesi ve sonrasındaki test bilgileri özetlenir ve iletilir.
- Bu rapor, test ilerleme raporu ve diğer verileri kullanır.
- Test ilerleme raporuna dayalı test metrikleri
- Sıradaki periyod için planlanan testler Versiyon v4.0 Test tamamlama raporu testin tamamlanması sırasında, bir proje, test seviyesi veya test çeşidi tamamlandığında ve ideal olarak çıkış kriterleri karşılandığında hazırlanır.
- Gerektiği zaman ve yerde yeni kaynaklar eklemek Versiyon v4.0 Test tamamlama, test projesinde elde edilen deneyimi, proje boyunca üretilen test çalışma ürünlerini ve elde edilen diğer ilgili bilgileri toplar ve bir araya getirir.

### Konfigürasyon Yönetimi

- Test öğeleri de dahil olmak üzere tüm yapılandırma öğelerinin benzersiz olarak tanımlanması, versiyon kontrolü yapılmış, değişiklikleri izlenmiş ve diğer yapılandırma öğeleriyle ilgili olması ve böylece test süreci boyunca izlenebilirliğinin sürdürülmesi
- Tanımlanan tüm dokümantasyon ve yazılım öğelerinin test çalışma ürünlerinde açık bir şekilde belirtilmesi Sürekli entegrasyon, sürekli teslimat, sürekli dağıtım ve ilgili testler genellikle otomatikleştirilmiş DevOps hattının (bkz. bölüm 2.1.4) bir parçası olarak uygulanır ve otomatikleştirilmiş YY de normalde buna dahildir.
- Yeni bir temel çizgi oluşturulduğunda, yapılandırma yönetimi değiştirilen yapılandırma öğelerinin bir kaydını tutar.
- Önceki test sonuçlarını yeniden üretmek için önceki temel çizgiye geri dönülebilir.

### Hata Yönetimi ve Hata Raporu

- Test nesnesinin ve test ortamının tanımı
- Anomalinin gözlemlendiği tarih, bildiren organizasyon ve yazar (rolü de dahil olmak üzere)
- Hatanın bağlamı (ör. çalıştırılan test senaryosu, yapılan test faaliyeti, YGYD aşaması ve test tekniği, kontrol listesi ve kullanılan test verisi gibi diğer ilgili bilgiler) Versiyon v4.0
- Anomaliyi tespit eden test adımları da dahil olmak üzere anomalinin yeniden oluşturulmasını ve çözümünü sağlamak üzere arızanın açıklaması, ilgili test kayıtları, veritabanı dökümleri, ekran görüntüleri veya kayıtlar
- Hatanın paydaşların çıkarları veya gereksinimler üzerindeki önem derecesi (etki derecesi)
- Düzeltilme önceliği
- Hatanın durumu (ör. açık, ertelenmiş, tekrarlanmış, düzeltilmeyi bekliyor, onaylama testi bekleniyor, yeniden açıldı, kapatıldı, reddedildi)
- Raporlanan hataları ele almaktan ve çözmekten sorumlu olanlara sorunu çözmek için yeterli bilgiyi sağlamak
- Referanslar (ör. test senaryosuna ilişkin) Bu verilerin bir kısmı hata yönetim araçları kullanıldığında otomatik olarak dahil edilebilir (ör. tanımlayıcı, tarih, yazar ve başlangıç durumu).

---

## Bölüm 6 — Test Araçları

### Yönetim ve Statik Test Araçları

- Yönetim araçları: YGYD yönetimini, gereksinimleri, testleri, hataları ve yapılandırmayı kolaylaştırarak test sürecinin verimliliğini artırır
- Statik test araçları: Gözden geçirmeler ve statik analiz konusunda test uzmanına destek sağlar

### Test Tasarımı ve Test Uygulama Araçları

- Test tasarımı ve test uygulama araçları: Test senaryoları, test verisi ve test prosedürlerini oluşturmayı kolaylaştırır

### Fonksiyonel Olmayan Test Araçları

- Fonksiyonel olmayan test araçları: Test uzmanının manuel olarak yapılması zor veya imkansız olan fonksiyonel olmayan testleri yapmasına olanak sağlar

### DevOps, CI/CD ve Altyapı Araçları

- DevOps araçları: DevOps teslimat hattını, iş akışı takibini, otomatik derleme süreçlerini, CI/CD'yi destekler
- Ölçeklenebilirliği ve dağıtım standardizasyonunu destekleyen araçlar (ör. sanal makineler, konteynerleştirme araçları)

### İş Birliği Araçları

- İş birliği araçları: İletişimi kolaylaştırır
