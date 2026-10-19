# Uludogan-Tech-Web-Bug-Report

# Uludoğan Tech - Web Site Quality Assurance & UI/UX Audit Report

Bu depo, Uludoğan Tech resmi web sitesi (`https://uludogantech.com`) üzerinde yapılan detaylı inceleme sırasında tespit edilen entegrasyon, yönlendirme, medya erişim hataları ve UI/UX (Kullanıcı Arayüzü / Deneyimi) eksikliklerini dökümante etmek amacıyla oluşturulmuştur.

## 🛠️ Test Ortamı (Environment)
- **Ana URL:** https://uludogantech.com
- **Cihaz/Tarayıcı:** Masaüstü & Mobil / Google Chrome (Güncel Sürüm)
- **Tarih:** 19 Ekim 2026
- **Testi Gerçekleştiren:** [Elif]

---

## 📌 Tespit Edilen Hatalar ve Analizler (Bug Summaries & UI/UX Issues)

### 🚨 1. Footer Menüsü Yanlış Yönlendirme Hatası (Redirection Bug)
- **Konum:** Sayfa Sonu (Footer / Altbilgi Menüsü)
- **Mevcut Durum:** Üst menüde (Header) yer alan proje linkleri doğru çalışırken, sayfanın en altında yer alan Footer menüsündeki **"Nano Sınıfta İnsansız Helikopter"** linki, kullanıcıyı hatalı bir rota (route) yönlendirmesiyle **"Yapay Zeka Destekli Uçuş Kontrol Kartı"** sayfasına götürmektedir.
- **Beklenen Durum:** Footer'daki linkin de tıpkı Header'daki gibi helikoptere ait doğru alt sayfaya yönlenmesi gerekir.
- **Şiddet (Severity):** Medium

### 🖼️ 2. "Basında Biz" Sayfası Kırık Görsel Hatası (Broken Image Bug)
- **Konum:** Üst Menü > Basında Biz Sayfası
- **Mevcut Durum:** *"Turkish Company Unveils NanoAlp Reconnaissance Microdrone"* başlıklı basın haberinin detayına girildiğinde, habere ait görseller yüklenmemekte (broken image icon) ve boş görünmektedir. (Görsel kaynak yolları veya sunucu izinleri kaynaklı hata).
- **Beklenen Durum:** Basın materyallerinin ve görsellerinin eksiksiz yüklenmesi gerekir.
- **Şiddet (Severity):** Medium

### 📹 3. Medya Oynatma ve Kırık Video Linkleri (Broken Video Media)
- **Konum:** Haberler / Basın Detay Sayfaları
- **Mevcut Durum:** Multimedya içeren diğer bazı haber sayfalarındaki video oynatıcılar (iframe / embedded video) yüklenmemekte, kaynak linkleri kırık olduğu için oynatma hatası vermektedir.
- **Beklenen Durum:** Haber içeriklerindeki video gömme kodlarının (YouTube/Vimeo vb.) API veya kaynak izinlerinin güncellenerek çalışır hale getirilmesi gerekir.
- **Şiddet (Severity):** Low-Medium

### 📐 4. Alt Sayfa Düzenleri ve Kullanıcı Deneyimi Eksiklikleri (UI/UX Layout Issues)
- **Konum:** Anasayfa Dışındaki Tüm Alt Sayfalar
- **Mevcut Durum:** Anasayfadaki tasarım özeni alt sayfalarda görülmemektedir. Alt sayfaların yerleşimi, kurumsal bir web sitesinden ziyade aceleyle hazırlanmış bir sunum slaytı (PowerPoint) mantığı taşımaktadır. Çok büyük başlıklar kullanılmasına rağmen içerik ve metinler son derece azdır. Sayfaların alt kısımları devasa boşluklar barındırmakta, bu da görsel dengeyi bozarak profesyonellik algısını olumsuz etkilemektedir.
- **Beklenen Durum:** Alt sayfaların modern UI/UX standartlarına uygun olarak grid sistemleri, açıklayıcı infografikler, ikonlar ve dengeli metin blokları ile zenginleştirilerek kurumsal kimliğe yakışır hale getirilmesi gerekir.
- **Şiddet (Severity):** UI/UX / Geliştirme Önerisi

---

## 💡 Teknik Çözüm Önerileri (Technical Recommendations)
1. Footer menüsündeki bileşenlerin `href` veya yönlendirme parametreleri kontrol edilerek doğru rota atanmalı.
2. Basın sayfasındaki medya kütüphanesi (media library) ve CDN linkleri kontrol edilerek eksik görseller sunucuya yeniden yüklenmeli.
3. Alt sayfalar için standart, boşlukları dolduran ve gözü yormayan modern bir sayfa şablonu (template) tasarlanmalı.
