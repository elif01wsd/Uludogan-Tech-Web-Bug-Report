# Uludogan-Tech-Web-Bug-Report

# Uludoğan Tech - Web Site Quality Assurance & UI/UX Audit Report

Bu depo, Uludoğan Tech resmi web sitesi (`https://uludogantech.com`) üzerinde yapılan detaylı inceleme sırasında tespit edilen entegrasyon, yönlendirme, medya erişim hataları ve UI/UX (Kullanıcı Arayüzü / Deneyimi) eksikliklerini dökümante etmek amacıyla oluşturulmuştur.

## 🛠️ Test Ortamı (Environment)
- **Ana URL:** https://uludogantech.com
- **Masaüstü Ortamı:** Windows 11 / Brave Browser (155.0.8059.85 - 64-bit)
- **Mobil Ortam:** Samsung Galaxy A26 (Android 14) / Brave Browser (155.0.8059.39)
- **Tarih:** 19 Ekim 2026
- **Testi Gerçekleştiren:** Elif

---

## 📌 Tespit Edilen Hatalar ve Analizler (Bug Summaries & UI/UX Issues)

### 🚨 1. Footer Menüsü Yanlış Yönlendirme Hatası (Redirection Bug)
- **Konum:** Sayfa Sonu (Footer / Altbilgi Menüsü)
- **Mevcut Durum:** Üst menüde (Header) yer alan proje linkleri doğru çalışırken, sayfanın en altında yer alan Footer menüsündeki **"Nano Sınıfta İnsansız Helikopter"** linki, kullanıcıyı hatalı bir rota (route) yönlendirmesiyle **"Yapay Zeka Destekli Uçuş Kontrol Kartı"** sayfasına götürmektedir.
- **Beklenen Durum:** Footer'daki linkin de tıpkı Header'daki gibi helikoptere ait doğru alt sayfaya yönlenmesi gerekir.
- **Şiddet (Severity):** Medium

  <img width="1912" height="965" alt="1" src="https://github.com/user-attachments/assets/2a23d88d-5718-4d1b-aae9-e9d958f86538" />


<img width="1902" height="957" alt="2" src="https://github.com/user-attachments/assets/d79ac0fd-be44-4cec-9df7-58df999ce7f7" />


### 🖼️ 2. "Basında Biz" Sayfası Kırık Görsel Hatası (Broken Image Bug)
- **Konum:** Üst Menü > Basında Biz Sayfası
- **Mevcut Durum:** *"Turkish Company Unveils NanoAlp Reconnaissance Microdrone"* başlıklı basın haberinin detayına girildiğinde, habere ait görseller yüklenmemekte (broken image icon) ve boş görünmektedir. (Görsel kaynak yolları veya sunucu izinleri kaynaklı hata).
- **Beklenen Durum:** Basın materyallerinin ve görsellerinin eksiksiz yüklenmesi gerekir.
- **Şiddet (Severity):** Medium

<img width="1915" height="957" alt="3" src="https://github.com/user-attachments/assets/a1a96040-295c-4751-82f4-827bedb8c970" />


### 📹 3. Medya Oynatma ve Kırık Video Linkleri (Broken Video Media)
- **Konum:** Haberler / Basın Detay Sayfaları
- **Mevcut Durum:** Multimedya içeren diğer bazı haber sayfalarındaki video oynatıcılar (iframe / embedded video) yüklenmemekte, kaynak linkleri kırık olduğu için oynatma hatası vermektedir.
- **Beklenen Durum:** Haber içeriklerindeki video gömme kodlarının (YouTube/Vimeo vb.) API veya kaynak izinlerinin güncellenerek çalışır hale getirilmesi gerekir.
- **Şiddet (Severity):** Low-Medium

<img width="1916" height="965" alt="4" src="https://github.com/user-attachments/assets/5c29515c-e187-4fa6-943c-5611213ddd3a" />


### 📐 4. Sayfa Düzenleri ve Kullanıcı Deneyimi Eksiklikleri (UI/UX Layout)
- **Konum:** Ana Sayfa Dışında Kalan Tüm Sayfalar (Hakkımızda, İletişim, Ürün Detayları vb.)
- **Mevcut Durum:** Ana sayfa dışındaki tüm sayfaların yerleşimi, kurumsal bir web sitesinden ziyade bir sunum slaytı (PowerPoint) mantığı taşımaktadır. Çok büyük başlıklar kullanılmasına rağmen içerik ve yazılar son derece azdır. Sayfaların yarısından fazlası boş kalmakta, bu da görsel dengeyi bozarak profesyonellik algısını olumsuz etkilemektedir.
- **Beklenen Durum:** Sayfaların modern UI/UX standartlarına uygun olarak dengeli metin blokları, ikonlar ve açıklayıcı ögelerle zenginleştirilerek kurumsal kimliğe yakışır hale getirilmesi gerekir.
- **Şiddet (Severity):** UI/UX / Geliştirme Önerisi


<img width="1917" height="967" alt="5" src="https://github.com/user-attachments/assets/970e5f31-19b7-49cf-986a-33ddc08206cb" />

---

## 💡 Teknik Çözüm Önerileri (Technical Recommendations)
1. Footer menüsündeki bileşenlerin `href` veya yönlendirme parametreleri kontrol edilerek doğru rota atanmalı.
2. Basın sayfasındaki medya kütüphanesi (media library) ve CDN linkleri kontrol edilerek eksik görseller sunucuya yeniden yüklenmeli.
3. Alt sayfalar için standart, boşlukları dolduran ve gözü yormayan modern bir sayfa şablonu (template) tasarlanmalı.
