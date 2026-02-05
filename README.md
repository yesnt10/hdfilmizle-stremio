# HDfilmizle Stremio Addon

Bu proje, **hdfilmizle.to** sitesinden film/dizi içeriklerini çekip Stremio üzerinde katalog + meta + stream olarak sunan bir Node.js eklentisidir.

> Not: Site tarafındaki HTML yapısı değiştikçe CSS selector’lar güncelleme isteyebilir.

## Özellikler

- Film kataloğu (`movie`)
- Dizi kataloğu (`series`)
- Arama (`extra.search`)
- İçerik detay/meta bilgisi
- Sayfadan iframe/video linkleri çıkarıp stream listesi üretme

## Kurulum

```bash
npm install
npm start
```

Varsayılan endpoint:

- `http://127.0.0.1:7000/manifest.json`

## Ortam Değişkenleri

- `PORT` (default: `7000`)
- `ADDON_ID` (default: `org.hdfilmizle.scraper`)
- `ADDON_NAME` (default: `HDfilmizle Scraper`)
- `HDFILMIZLE_BASE_URL` (default: `https://www.hdfilmizle.to`)
- `REQUEST_TIMEOUT_MS` (default: `15000`)
- `MAX_CATALOG_ITEMS` (default: `80`)
- `HTTP_USER_AGENT` (opsiyonel)

## Stremio’ya Ekleme

1. Eklentiyi çalıştır.
2. Tarayıcıdan `manifest.json` URL’ini aç.
3. Stremio “Add addon” ile URL’i ekle.

## Önemli

Bu eklenti scraping mantığıyla çalışır. Eğer stream linkleri dinamik JS ile üretilirse veya anti-bot koruması aktifse doğrudan link çıkarmak zorlaşabilir. Bu durumda selector/parsing güncellemesi gerekir.
