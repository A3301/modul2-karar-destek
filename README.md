# Modül 2: Karar Destek Sistemleri ve Tahminleyici Modelleme

**Sağlık Bilimleri Fakültesi · Öğretim Elemanları için Yapay Zekâ Eğitimi** · Eğitmen: Ali AKDAĞLI · 12 saat (4 oturum)

Değerli hocalarım, hoş geldiniz.

Bu sayfada Modül 2 için hazırladığımız her şeyi bir arada bulacaksınız. Önümüzdeki dört oturumda, bir yapay zekâ modelinin ekrana koyduğu risk tahminini bir laboratuvar sonucunu okur gibi birlikte okumayı deneyeceğiz.

“Duyarlılık, PPV, AUC” gibi kavramlar ilk bakışta teknik görünebilir; aslında hepimizin klinikte her gün kullandığı tanı testi mantığına çok benziyorlar. Kod yazmayacağız, formül ezberlemeyeceğiz; merakınız ve klinik deneyiminiz fazlasıyla yeterli.

Kendi araştırmalarınızda ve öğrencilerinizle yürüttüğünüz çalışmalarda bu bakışın çok işinize yarayacağına inanıyorum. Görüşmek üzere. — *Ali AKDAĞLI*

Materyaller bilgisayar ve tablette en rahat okunur; bu sayfa telefonda da rahatça açılır. Hiçbir belgeyi yazdırmanıza gerek yok; PDF’leri kendi cihazınızda açmanız yeterli.

Random Forest, XGBoost gibi algoritmaların çıktılarını klinik olarak okumayı öğreniyoruz: duyarlılık, PPV, ROC/AUC, kalibrasyon ve SHAP. Sepsis, diyabet komplikasyonları, malnütrisyon ve preeklampsi örnekleriyle.

## En kolay kullanım
- **Web sayfası (telefon dahil):** `https://A3301.github.io/modul2-karar-destek/` adresini açalım. Ana ekrana ekleyerek uygulama gibi kullanabilirsiniz.
- **Hepsini indirmek:** Bu sayfada yeşil **Code** düğmesi → **Download ZIP**. ZIP'i açalım ve `index.html` dosyasına çift tıklayalım. Kurulum gerekmez.

## Kursa gelmeden önce
- [ ] Uygulamalar için dizüstü ya da masaüstü bilgisayar (Windows veya macOS) ve şarj aleti. Orange tablet ve telefonda çalışmadığı için, tablet ya da telefonla katılan hocalarımız uygulamaları perdeden ve ders notundaki ekran çizimlerinden rahatça izleyebilir.
- [ ] Orange Data Mining'i orangedatamining.com/download adresinden indirip kuralım.
- [ ] Orange'ı açalım: Options → Add-ons → listeden "Explain" işaretleyelim → OK. Orange'ı kapatıp yeniden açalım.
- [ ] Bu sayfadaki 5 veri dosyasını bilgisayarınıza indirelim (tek seferde: GitHub sayfasında Code → Download ZIP).
- [ ] Kodlama bilgisi gerekmez. Duyarlılık ve özgüllük kavramlarını hatırlamanız yeterli.

## Orange kurulumu adım adım
1. orangedatamining.com/download adresine gidelim, işletim sisteminize uygun yükleyiciyi indirelim.
2. Windows: indirilen .exe dosyasını çalıştırıp "İleri" diyerek kuralım. macOS: .dmg dosyasını açıp Orange'ı Uygulamalar klasörüne sürükleyelim.
3. Orange'ı açalım. Üst menüden Options → Add-ons… seçelim.
4. Listede "Explain" eklentisini işaretleyip OK'e basalım; kurulum bitince Orange'ı yeniden başlatalım.
5. Deneme: soldaki "File" bileşenini tuvale sürükleyelim, çift tıklayalım ve sepsis_sentetik.csv dosyasını açalım. Tabloyu görüyorsanız hazırsınız.

## İçerik
| Dosya | Açıklama |
|---|---|
| `index.html` | Tüm materyallere tek sayfadan erişim |
| `belgeler/Modul2_Ders_Notu.pdf` | Ders notu – Kısaltma kartları, tıbbi terim kutuları, çözümlü hesaplar ve sözlükler. |
| `belgeler/Modul2_Katilimci_Sunumu.pdf` | Sunum – Derste kullanılan slaytlar. |
| `veri/sepsis_sentetik.csv` | Sepsis (24 saat), 3000 servis hastası · sentetik |
| `veri/diyabet_pima.csv` | Diyabet, 768 Pima yerlisi kadın · gerçek açık veri |
| `veri/diyabetik_ayak_sentetik.csv` | Diyabetik ayak ülseri (12 ay), 2000 hasta · sentetik |
| `veri/malnutrisyon_sentetik.csv` | Malnütrisyon (GLIM), 1500 yaşlı hasta · sentetik |
| `veri/preeklampsi_sentetik.csv` | Preeklampsi, 4000 gebe (11–13. hafta) · sentetik |


**Veri kaynakları:** `diyabet_pima.csv`, Pima Indians Diabetes veri setidir (Smith JW ve ark., 1988; OpenML kimlik 37); fizyolojik olarak imkânsız sıfır değerleri eksik veri olarak kodlanmıştır. Diğer dört veri seti eğitim için üretilmiş sentetik verilerdir.

> Kurs boyunca yalnızca eğitim için hazırlanmış sentetik verilerle çalışmayı öneriyoruz; böylece hem hastalarımızın hem de katılımcılarımızın bilgileri güvende kalır (6698 sayılı KVKK).
