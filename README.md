# Portfolio Muhammad Haikal Fanzury

Website portfolio dinamis untuk GitHub Pages. Tampilan tetap diatur oleh HTML/CSS, sedangkan isi portfolio bisa diambil dari Google Sheets yang dipublish sebagai CSV.

## Isi Folder

- `index.html` - struktur utama halaman.
- `styles.css` - desain, layout, dan responsif.
- `script.js` - renderer dinamis dari data spreadsheet.
- `site-config.js` - tempat menaruh URL CSV Google Sheets.
- `spreadsheet-template.csv` - template kolom untuk Google Sheets.
- `CUSTOMIZE.md` - panduan mengubah warna, posisi foto, dan layout kecil dari spreadsheet.
- `assets/` - foto profil, screenshot proyek, dan gambar galeri.
- `.nojekyll` - agar GitHub Pages menyajikan file statis apa adanya.

## Cara Deploy ke GitHub Pages

1. Upload seluruh isi folder ini ke repository GitHub.
2. Buka `Settings` repository.
3. Masuk ke `Pages`.
4. Pada `Build and deployment`, pilih:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/root`
5. Klik `Save`.

URL biasanya berbentuk:

```text
https://username.github.io/nama-repository/
```

## Cara Menghubungkan Google Sheets

1. Buka `spreadsheet-template.csv`.
2. Import atau salin isinya ke Google Sheets.
3. Di Google Sheets, pilih `File > Share > Publish to web`.
4. Pilih sheet data utama.
5. Pilih format `Comma-separated values (.csv)`.
6. Klik `Publish`, lalu copy URL CSV-nya.
7. Buka `site-config.js`.
8. Tempel URL ke bagian ini:

```js
window.PORTFOLIO_CONFIG = {
  spreadsheetCsvUrl: "TEMPEL_URL_CSV_DI_SINI",
  cacheBustSpreadsheet: true
};
```

9. Upload ulang `site-config.js` ke GitHub.

Setelah itu, update isi Google Sheets akan otomatis muncul di website saat halaman dibuka ulang. Tidak perlu upload ulang GitHub selama yang berubah hanya teks/link/data di spreadsheet.

## Format Section

Gunakan nilai berikut di kolom `section`:

- `setting` - teks umum seperti nama, headline, email, WhatsApp.
- `stat` - angka highlight di bawah hero.
- `work` - histori pekerjaan.
- `education` - histori pendidikan.
- `project` - kartu portfolio projek utama.
- `project_history` - riwayat projek tambahan.
- `skill` - update skill.
- `certification` - sertifikasi.
- `gallery` - gambar galeri.
- `contact` - tombol kontak.

## Catatan Penting

- Kolom `order` menentukan urutan tampil.
- Kolom `visible` bisa diisi `TRUE` atau `FALSE`.
- Untuk daftar seperti skill, tools, atau bullet point, pisahkan item dengan tanda `|`.
- Gambar boleh memakai path lokal seperti `assets/monthly-dashboard.jpg` atau URL gambar publik.
- Kalau menambah gambar baru ke folder `assets`, file gambar tetap harus diupload ke GitHub.
- Jangan isi data rahasia di Google Sheets, karena sheet yang dipublish bisa dibaca publik.
