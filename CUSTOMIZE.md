# Panduan Customisasi Tampilan

Mulai versi ini, spreadsheet hanya untuk konten. Tampilan website diatur dari file `styles.css`.

Gunakan file berikut saat ingin meminta AI lain memperbaiki desain:

- `index.html`
- `styles.css`
- `script.js`
- `STYLE-GUIDE.md`
- `style-guide.csv`

## Bagian Yang Paling Sering Diubah

| Tujuan | File | Selector utama |
| --- | --- | --- |
| Warna global | `styles.css` | `:root` |
| Hero dan foto utama | `styles.css` | `.hero`, `.hero-grid`, `.portrait-stage` |
| Statistik/counter | `styles.css`, `script.js` | `.proof-grid`, `.stat-value`, `prepareCounters()` |
| Animasi saat scroll | `styles.css`, `script.js` | `.reveal-on-scroll`, `prepareScrollReveals()` |
| Kartu project | `styles.css`, `script.js` | `.project-card`, `renderProjects()` |
| Galeri dan lightbox | `styles.css`, `script.js` | `.gallery-item`, `.lightbox`, `createMediaFigure()` |
| Histori project | `styles.css`, `script.js` | `.history-list`, `renderProjectHistory()` |

## Cara Aman Meminta AI Lain Upgrade CSS

Gunakan prompt seperti ini:

```text
Tolong upgrade tampilan portfolio ini agar lebih modern dan interaktif.
Pertahankan format spreadsheet, data-render, data-field, dan fungsi JavaScript yang sudah ada.
Jangan pindahkan style ke spreadsheet.
Fokus pada hero, animated counter, reveal on scroll, project card, gallery lightbox, dan mobile responsive.
```

## Catatan

- Baris `style_...` di spreadsheet sudah tidak diperlukan.
- Jika hanya mengubah teks/konten, cukup edit Google Sheets.
- Jika mengubah desain, upload ulang `styles.css`.
- Jika mengubah animasi/interaksi, upload ulang `script.js`.
