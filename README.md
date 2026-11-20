# caniasERP Excel Builder

caniasERP'nin PostgreSQL veritabanından, son kullanıcının düzenleyip ERP'ye geri gönderebileceği **korumalı Excel şablonları** üreten masaüstü uygulaması. Veritabanına yalnızca okuma yetkisiyle bağlanır.

> Bu depo bir proje vitrinidir. Kaynak kod paylaşılmamaktadır.

## Problem

Toplu veri güncellemesi (fiyat, müşteri bilgisi, malzeme kartı vb.) ERP ekranlarında satır satır yapıldığında saatler sürüyordu. Bu araç kullanıcıya güvenli bir Excel şablonu verir. Kullanıcı yalnızca izin verilen alanları değiştirebilir. Doldurulan dosya bir Power Automate akışı ve ERP web servisi üzerinden sisteme geri yazılır.

## Özellikler

- Şema ve tablo arama, sütunları otomatik getirme
- Sütun sınıflandırma: **Anahtar**, **Düzenlenebilir**, **Salt okunur**, **Dahil etme**. Birincil anahtarlar otomatik tanınır.
- SQL filtreleriyle satırları daraltma ve satır sayısı uyarısı
- Tablo bazında yapılandırma ve bağlantı profili kaydetme
- Üretilen Excel'in yapısı:
  - Gerçek bir Excel Table nesnesi
  - Korumalı sayfa, kilidi yalnızca düzenlenebilir sütunlarda açık
  - `Durum` / `Mesaj` / `SonIslem` / `Versiyon` kontrol sütunları ve açılır listeler
  - Geri yazma akışı için meta veri sayfası
- PyInstaller ile tek dosyalık, konsolsuz `.exe`

## Teknolojiler

`Python` · `Tkinter` · `psycopg2` · `openpyxl` · `PyInstaller` · `Power Automate` · `PostgreSQL`
