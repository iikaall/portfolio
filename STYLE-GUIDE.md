# Panduan Upgrade CSS

Spreadsheet sekarang difokuskan untuk konten. CSS tidak lagi dikendalikan dari baris `style_...` di spreadsheet.

Jika ingin meminta AI lain upgrade tampilan, berikan file berikut:

- `index.html`
- `styles.css`
- `script.js`
- `STYLE-GUIDE.md`
- `style-guide.csv`

## Referensi Arah Visual

Inspirasi dari `https://crosslife.id/` yang relevan untuk portfolio ini:

- Statistik yang naik dari `0` ke angka asli saat discroll.
- Elemen section/kartu muncul halus saat masuk viewport.
- Layout landing page yang terasa interaktif, bukan halaman statis.
- Card project/portfolio yang bisa dibuka untuk melihat detail.
- Galeri visual yang bisa diklik untuk preview besar.

## Batas Aman Saat Upgrade

- Jangan mengubah nama atribut `data-render` dan `data-field` di `index.html`.
- Jangan mengubah format kolom spreadsheet tanpa update `script.js`.
- Jangan menghapus fungsi `renderPortfolio`, `rowsToPortfolio`, dan `loadSpreadsheetData`.
- Boleh mengubah tampilan di `styles.css`.
- Boleh menambah animasi di `script.js` selama data spreadsheet tetap terbaca.

## Bagian Penting CSS

| Bagian | Selector utama | Fungsi |
| --- | --- | --- |
| Hero | `.hero`, `.hero-grid`, `.portrait-stage` | First screen, foto, background grid |
| Statistik | `.proof-band`, `.proof-grid`, `.stat-value` | Counter dan angka highlight |
| Project | `.project-card`, `.project-media`, `.project-extra` | Card project dan detail |
| Histori project | `.history-list`, `.history-toggle`, `.history-detail` | List project compact |
| Galeri | `.gallery-grid`, `.gallery-item`, `.lightbox` | Grid gambar/video dan preview |
| Animasi scroll | `.reveal-on-scroll`, `.is-visible` | Efek muncul saat digulir |

## Prompt Singkat Untuk AI Lain

```text
Tolong upgrade CSS portfolio ini agar terasa seperti landing page interaktif modern.
Pertahankan struktur HTML dan format spreadsheet yang sudah ada.
Fokus pada hero, animated counter, reveal on scroll, project cards, gallery lightbox, dan responsive mobile.
Jangan pindahkan pengaturan style ke spreadsheet.
```
