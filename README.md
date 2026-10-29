# Modül 2: Karar Destek Sistemleri ve Tahminleyici Modelleme

**Tarsus Üniversitesi Sağlık Bilimleri Fakültesi · Öğretim Üyelerine Yapay Zekâ Eğitimi** · Eğitmen: Ali AKDAĞLI · 12 saat (4 oturum)

Random Forest, XGBoost gibi algoritmaların çıktılarını klinik olarak okumayı öğreniyoruz: duyarlılık, PPV, ROC/AUC, kalibrasyon ve SHAP. Sepsis, diyabet komplikasyonları, malnütrisyon ve preeklampsi örnekleriyle.

## En kolay kullanım
- **Web sayfası (telefon dahil):** `https://A3301.github.io/modul2-karar-destek/` adresini açın. Ana ekrana ekleyerek uygulama gibi kullanabilirsiniz.
- **Hepsini indirmek:** Bu sayfada yeşil **Code** düğmesi → **Download ZIP**. ZIP'i açın ve `index.html` dosyasına çift tıklayın. Kurulum gerekmez.

## Kursa gelmeden önce
- [ ] Dizüstü bilgisayar (Windows veya macOS) ve şarj aleti. Orange tablet ve telefonda çalışmaz.
- [ ] Orange Data Mining'i orangedatamining.com/download adresinden indirip kurun.
- [ ] Orange'ı açın: Options → Add-ons → listeden "Explain" işaretleyin → OK. Orange'ı kapatıp yeniden açın.
- [ ] Bu sayfadaki 5 veri dosyasını bilgisayarınıza indirin (tek seferde: GitHub sayfasında Code → Download ZIP).
- [ ] Kodlama bilgisi gerekmez. Duyarlılık ve özgüllük kavramlarını hatırlamanız yeterli.

## Orange kurulumu adım adım
1. orangedatamining.com/download adresine gidin, işletim sisteminize uygun yükleyiciyi indirin.
2. Windows: indirilen .exe dosyasını çalıştırıp "İleri" diyerek kurun. macOS: .dmg dosyasını açıp Orange'ı Uygulamalar klasörüne sürükleyin.
3. Orange'ı açın. Üst menüden Options → Add-ons… seçin.
4. Listede "Explain" eklentisini işaretleyip OK'e basın; kurulum bitince Orange'ı yeniden başlatın.
5. Deneme: soldaki "File" bileşenini tuvale sürükleyin, çift tıklayın ve sepsis_sentetik.csv dosyasını açın. Tabloyu görüyorsanız hazırsınız.

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

> Kurs boyunca hiçbir YZ aracına gerçek hasta veya katılımcı verisi yazmayın (6698 sayılı KVKK).
