# Panduan Customisasi Tampilan

Website ini bisa dikustom dari Google Sheets melalui baris `section = setting` dan `key` yang diawali `style_`.

Untuk perubahan kecil, kamu tidak perlu membuka CSS. Cukup ubah kolom `value` pada baris style di spreadsheet.

## Cara Pakai

1. Buka Google Sheets portfolio.
2. Cari baris dengan `key` diawali `style_`.
3. Ubah kolom `value`.
4. Refresh website.

Jika belum ada barisnya, tambahkan baris baru:

```text
section: setting
visible: TRUE
key: style_hero_photo_y
value: -24px
```

## Pengaturan Paling Sering Dipakai

| Key | Efek | Contoh nilai |
| --- | --- | --- |
| `style_background` | Warna background utama website | `#fbfaf6` |
| `style_background_alt` | Background section resume | `#f2efe7` |
| `style_text` | Warna teks utama | `#172126` |
| `style_primary` | Warna aksen hijau/teal | `#0f8b8d` |
| `style_primary_dark` | Warna section kontak | `#0a5e61` |
| `style_accent` | Warna aksen kuning | `#f5b942` |
| `style_coral` | Warna aksen merah | `#e85d5d` |
| `style_blue` | Warna bayangan biru | `#315c9b` |
| `style_section_padding` | Jarak atas-bawah tiap section | `92px` |
| `style_card_radius` | Lengkung sudut kartu | `8px` |

## Mengatur Foto Hero

| Key | Efek | Contoh nilai |
| --- | --- | --- |
| `style_hero_photo_y` | Naik/turun foto utama. Nilai negatif naik. | `-24px` |
| `style_hero_photo_scale` | Membesarkan/mengecilkan foto utama | `1.05` |
| `style_hero_photo_width` | Lebar area foto di desktop | `360px` |
| `style_hero_photo_min_height` | Tinggi area foto desktop | `410px` |
| `style_hero_photo_max_height` | Tinggi maksimal foto desktop | `455px` |
| `style_hero_photo_tablet_min_height` | Tinggi area foto tablet | `400px` |
| `style_hero_photo_mobile_min_height` | Tinggi area foto mobile | `340px` |
| `style_hero_photo_mobile_max_height` | Tinggi maksimal foto mobile | `380px` |

Rekomendasi aman:

- Foto ingin naik sedikit: `style_hero_photo_y = -16px`
- Foto ingin turun sedikit: `style_hero_photo_y = 16px`
- Foto ingin sedikit lebih besar: `style_hero_photo_scale = 1.05`
- Foto ingin sedikit lebih kecil: `style_hero_photo_scale = 0.95`

## Mengatur Background Foto Hero

| Key | Efek | Contoh nilai |
| --- | --- | --- |
| `style_hero_photo_bg_width` | Ukuran kotak background foto | `82%` |
| `style_hero_photo_bg_right` | Posisi kotak dari kanan | `5%` |
| `style_hero_photo_bg_bottom` | Posisi kotak dari bawah | `8%` |
| `style_hero_photo_bg_color_1` | Warna segitiga/kotak pertama | `#f5b942` |
| `style_hero_photo_bg_color_2` | Warna kotak kedua | `#0f8b8d` |
| `style_hero_photo_bg_shadow` | Bayangan kotak foto | `18px 18px 0 #e85d5d` |

Contoh agar background lebih pas dengan foto:

```text
style_hero_photo_bg_width = 76%
style_hero_photo_bg_bottom = 12%
style_hero_photo_y = -20px
```

## Mengatur Hero dan Judul

| Key | Efek | Contoh nilai |
| --- | --- | --- |
| `style_hero_padding_top` | Jarak atas hero desktop | `64px` |
| `style_hero_padding_bottom` | Jarak bawah hero desktop | `54px` |
| `style_hero_mobile_padding_top` | Jarak atas hero mobile | `48px` |
| `style_hero_gap` | Jarak antara teks dan foto desktop | `76px` |
| `style_hero_title_max_size` | Ukuran maksimal nama di desktop | `6.15rem` |
| `style_hero_title_mobile_max_size` | Ukuran maksimal nama di mobile | `4.5rem` |
| `style_hero_dark_height` | Tinggi bidang gelap bawah hero | `42%` |
| `style_hero_dark_slope` | Kemiringan bidang gelap | `28%` |

## Mengatur Thumbnail Navbar

| Key | Efek | Contoh nilai |
| --- | --- | --- |
| `style_brand_photo_y` | Posisi crop foto kecil di navbar | `18%` |
| `style_brand_photo_scale` | Zoom foto kecil di navbar | `1.35` |

Jika wajah terlalu turun di thumbnail:

```text
style_brand_photo_y = 10%
```

Jika wajah terlalu dekat:

```text
style_brand_photo_scale = 1.15
```

## Catatan Aman

- Untuk warna, pakai format hex seperti `#0f8b8d`.
- Untuk ukuran, pakai `px`, misalnya `24px`.
- Untuk persentase, pakai `%`, misalnya `42%`.
- Untuk skala foto, pakai angka tanpa satuan, misalnya `1.05`.
- Jangan mengubah `section`, `key`, atau nama kolom jika tidak perlu.
- Jika tampilan terasa rusak, kosongkan value style yang baru kamu ubah atau kembalikan ke nilai contoh di `spreadsheet-template.csv`.
