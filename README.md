# Modül 2: Karar Destek Sistemleri ve Tahminleyici Modelleme

**Sağlık Bilimleri Fakültesi · Öğretim Elemanları için Yapay Zekâ Eğitimi** · Eğitmen: Ali AKDAĞLI · 12 saat (4 oturum)

Random Forest, XGBoost gibi algoritmaların çıktılarını klinik olarak okumayı öğreniyoruz: duyarlılık, PPV, ROC/AUC, kalibrasyon ve SHAP. Sepsis, diyabet komplikasyonları, malnütrisyon ve preeklampsi örnekleriyle.

## En kolay kullanım
- **Web sayfası (telefon dahil):** `https://A3301.github.io/modul2-karar-destek/` adresinden erişilebilir. Sayfa, ana ekrana eklenerek uygulama gibi kullanılabilir.
- **Hepsini indirmek:** Bu sayfada yeşil **Code** düğmesi → **Download ZIP**. ZIP dosyası açıldıktan sonra `index.html` dosyası çift tıklanarak görüntülenir. Kurulum gerekmez.

## Kursa gelmeden önce
- [ ] Uygulamalar için dizüstü ya da masaüstü bilgisayar (Windows veya macOS) ve şarj aleti. Orange tablet ve telefonda çalışmadığından, bu cihazlarla katılım hâlinde uygulamalar perdeden ve ders notundaki ekran çizimlerinden izlenebilir.
- [ ] Orange Data Mining, orangedatamining.com/download adresinden indirilerek kurulur.
- [ ] Orange açıldıktan sonra Options → Add-ons menüsünden "Explain" eklentisi işaretlenir ve OK ile onaylanır; ardından program yeniden başlatılır.
- [ ] Bu sayfadaki 5 veri dosyası bilgisayara indirilir (tümü için: GitHub sayfasında Code → Download ZIP).
- [ ] Kodlama bilgisi gerekmez; duyarlılık ve özgüllük kavramlarına aşinalık yeterlidir.

## Orange kurulumu adım adım
1. orangedatamining.com/download adresinden işletim sistemine uygun yükleyici indirilir.
2. Windows: indirilen .exe dosyası çalıştırılır ve "İleri" adımlarıyla kurulum tamamlanır. macOS: .dmg dosyası açılır ve Orange, Uygulamalar klasörüne taşınır.
3. Orange açılır; üst menüden Options → Add-ons… seçilir.
4. Listede "Explain" eklentisi işaretlenip OK ile onaylanır; kurulum tamamlandığında Orange yeniden başlatılır.
5. Kontrol: soldaki "File" bileşeni tuvale taşınır, çift tıklanır ve sepsis_sentetik.csv dosyası açılır. Tablo görüntüleniyorsa kurulum tamamlanmıştır.

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
