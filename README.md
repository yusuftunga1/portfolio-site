# Yusuf Tunga

Kaydırdıkça açılan sinematik kişisel site. Ziyaretçi aşağı kaydırdıkça kahraman video da
aynı yönde ilerliyor, yukarı kaydırdıkça geri sarıyor. Sayfa videonun durduğu yerde
yerleşiyor ve altında gerçek bir web sitesi başlıyor.

Web ve mobil ürün geliştirici. Fikirden yayına, katman katman.

## Ne var burada

Tek `index.html` ve bir `assets` klasörü. Çerçeve yok, derleme adımı yok, npm yok.
Dosyayı sunucuya kopyalamak siteyi yayına almak için yeterli.

## Öne çıkanlar

- **Kaydırmaya bağlı kahraman video.** Kaydırma konumu videonun zamanına birebir bağlanıyor.
  Video tarayıcıya Blob olarak indiriliyor, çünkü bazı sunucular parçalı indirmeyi
  desteklemiyor ve o durumda ileri sarma çalışmıyor.
- **Telefonda video yok.** Küçük ekranlar, dikey tabletler ve azaltılmış hareket tercihi
  olan ziyaretçiler tasarlanmış sabit bir görsel görüyor ve videodan tek bayt indirmiyor.
  Beş koşulun tamamı hem CSS'te hem JavaScript'te birebir aynı yazılı, ekran döndüğünde
  ya da pencere yeniden boyutlandığında canlı olarak yeniden karar veriliyor.
- **Okunabilirlik ölçülerek yapıldı.** Videonun üstündeki her yazı bloğu, o bloğun
  gösterildiği en parlak kareye karşı ölçüldü. En düşük kontrast 4,2 olacak şekilde
  perde koyulukları kare kare ayarlandı.
- **Video gelmese de sayfa tam.** Video indirilemezse poster görsel kalıyor, yükleme
  halkasının yerini kaydırma işareti alıyor ve site eksiksiz çalışmaya devam ediyor.
- **Hareket her yerde ama fısıltı seviyesinde.** Her bölümün kendine ait bir girişi var,
  hiçbir şey zıplamıyor, hiçbir döngü sekme arkada kalırken çalışmıyor.
- **Erişilebilirlik.** İçeriğe atlama bağlantısı, gerçek başlık hiyerarşisi, klavye
  odağı için görünür halka, dokunmatikte en az 44 piksel hedef alanı, süsleme
  öğeleri ekran okuyucudan gizli.

## Teknik

| | |
|---|---|
| Diller | HTML, CSS, JavaScript (çerçevesiz) |
| Derleme | Yok |
| Yazı tipleri | Sora, Source Sans 3, JetBrains Mono |
| Sayfa boyutu | 45 KB (video hariç) |
| Video | 6 saniye, 720p, 2,4 MB, 8 karede bir anahtar kare |

Video `-g 8 -keyint_min 8` ile kodlandı. Tarayıcı sadece anahtar karelere tam olarak
atlayabildiği için, kısa anahtar kare aralığı kaydırmanın takılmadan akmasını sağlıyor.

## Yerelde çalıştırma

Sayfayı çift tıklayarak açabilirsin, ama tarayıcılar `file://` adreslerinde `fetch`
çağrısını engellediği için video yüklenmez ve tasarlanmış sabit görsel görünür.
Kaydırmalı hali görmek için klasörü küçük bir sunucuyla aç:

```bash
npx http-server . -p 5173 -c-1
```

Sonra tarayıcıda `http://localhost:5173` adresini aç. Python varsa şu da olur:

```bash
python -m http.server 5173
```

## Klasör yapısı

```
.
├── index.html              tüm sayfa, stiller ve betikler
└── assets
    ├── hero-scrub.mp4      kaydırmaya bağlı kahraman video
    ├── hero-poster.jpg     videonun ilk karesi
    └── hero-ending.jpg     videonun son karesi, telefon kahramanı ve tasarım görseli
```

## Telif

Bu depodaki içerik ve tasarım Yusuf Tunga'ya aittir.

---

**English:** A cinematic, scroll driven personal site. The hero video is scrubbed by scroll
position, small screens get a designed static hero instead and download no video at all, and
the whole thing is plain HTML, CSS and JavaScript with no build step. Serve the folder with
any static server.
