<div align="center">

# 🎬 Yusuf Tunga — Cinematic Scroll Personal Website

[![Live Website](https://img.shields.io/badge/Website-yusuftunga1.github.io/portfolio--site-5CC8E8.svg?style=for-the-badge&logo=google-chrome&logoColor=white)](https://yusuftunga1.github.io/portfolio-site/)
[![License: MIT](https://img.shields.io/badge/License-MIT-00ff88.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)](https://en.wikipedia.org/wiki/HTML5)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6.svg?style=for-the-badge&logo=css3&logoColor=white)](https://en.wikipedia.org/wiki/CSS)
[![JavaScript](https://img.shields.io/badge/Vanilla_JS-F7DF1E.svg?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

[🚀 Canlı Siteyi Aç](https://yusuftunga1.github.io/portfolio-site/) · [🌌 3D Portfolyoyu İncele](https://github.com/yusuftunga1/3d-portfolio) · [✨ Öne Çıkanlar](#-öne-çıkanlar) · [🛠️ Teknik](#-teknik)

</div>

---

Kaydırdıkça açılan sinematik kişisel site. Ziyaretçi aşağı kaydırdıkça kahraman video da aynı yönde ilerliyor, yukarı kaydırdıkça geri sarıyor. Sayfa videonun durduğu yerde yerleşiyor ve altında gerçek bir web sitesi başlıyor.

> **Web ve mobil ürün geliştirici.** Fikirden yayına, katman katman.

---

## 📦 Ne var burada?

Tek `index.html` ve bir `assets` klasörü. Çerçeve yok, derleme adımı yok, npm bağımlılığı yok.  
Dosyayı sunucuya kopyalamak siteyi yayına almak için yeterli.

---

## ✨ Öne Çıkanlar

- 🎥 **Kaydırmaya Bağlı Kahraman Video:** Kaydırma konumu videonun zamanına birebir bağlanıyor. Video tarayıcıya Blob olarak indiriliyor, böylece tüm sunucularda kusursuz ileri/geri sarma sağlanıyor.
- 📱 **Mobil Uyumluluk & Tasarruf:** Küçük ekranlar, dikey tabletler ve azaltılmış hareket tercihi olan ziyaretçiler tasarlanmış sabit bir görsel görüyor ve videodan tek bayt veri indirmiyor.
- 👁️ **Ölçülü Okunabilirlik:** Videonun üstündeki her yazı bloğu, o bloğun gösterildiği en parlak kareye karşı ölçüldü. En düşük kontrast 4,2 olacak şekilde perde koyulukları kare kare ayarlandı.
- 🛡️ **Hata Toleransı:** Video indirilemezse poster görsel kalıyor, yükleme halkasının yerini kaydırma işareti alıyor ve site eksiksiz çalışmaya devam ediyor.
- ♿ **Erişilebilirlik:** İçeriğe atlama bağlantısı, gerçek başlık hiyerarşisi, klavye odağı için görünür halka, dokunmatikte en az 44 piksel hedef alanı.

---

## 🛠️ Teknik Özellikler

| Özellik | Değer |
|---|---|
| **Diller** | HTML, CSS, JavaScript (Vanilla / Çerçevesiz) |
| **Derleme (Build)** | Yok (Doğrudan çalışır) |
| **Yazı Tipleri** | *Sora*, *Source Sans 3*, *JetBrains Mono* |
| **Sayfa Boyutu** | ~45 KB (video hariç) |
| **Video Formatı** | 6 saniye, 720p, 2.4 MB, 8 karede bir anahtar kare (`-g 8 -keyint_min 8`) |

---

## 🚀 Yerelde Çalıştırma

Sayfayı doğrudan tarayıcıda açabilir veya yerel bir statik sunucuyla çalıştırabilirsiniz:

```bash
# Python ile
python3 -m http.server 5173

# Veya Node ile
npx http-server . -p 5173 -c-1
```

Ardından tarayıcınızda `http://localhost:5173` adresine gidebilirsiniz.

---

## 📂 Klasör Yapısı

```
.
├── index.html              # Tüm sayfa, stiller ve betikler
├── LICENSE                 # MIT Açık Kaynak Lisansı
├── README.md               # Proje dokümantasyonu
└── assets/
    ├── hero-scrub.mp4      # Kaydırmaya bağlı kahraman video
    ├── hero-poster.jpg     # Videonun ilk karesi
    └── hero-ending.jpg     # Videonun son karesi & telefon kahramanı
```

---

## 🌌 Diğer Projeler

- ⚡ **[3d-portfolio](https://github.com/yusuftunga1/3d-portfolio)**: React 19, Three.js ve Tailwind CSS v4 ile geliştirilmiş etkileşimli 3D parçacık ve WebGL portfolyosu ([Canlı Demo](https://yusuftunga1.github.io/3d-portfolio/)).

---

## 📜 Lisans

Bu proje [MIT Lisansı](LICENSE) ile lisanslanmıştır.

---

<div align="center">

Crafted with 💙 by [**Yusuf Tunga**](https://github.com/yusuftunga1)

</div>
