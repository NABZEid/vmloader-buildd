# VMloader-spaceman

Create by SpacemanBuilder. Auto play Vita Mahjong dengan jendela mengambang.

## Build di GitHub

1. Buat repo baru, upload semua isi folder ini (termasuk folder `.github`).
2. Buka tab **Actions** > **Build VMloader-spaceman** > **Run workflow**.
3. Setelah selesai, unduh artifact **VMloader-spaceman** (isinya `VMloader-spaceman.apk`).

## Pasang dan pakai

1. Buka aplikasi, izinkan **Tampil di atas aplikasi lain**.
2. Aktifkan **VMloader-spaceman** di Pengaturan > Aksesibilitas.
3. Tekan **Tampilkan jendela mengambang**, lalu buka Vita Mahjong.
4. Ketuk logo mengambang, isi **Target level** (0 = unlimited), tekan **Auto Play**.
5. Ketuk logo lagi lalu **Stop** untuk berhenti.

Target level dihitung dari jumlah level yang selesai sejak Auto Play ditekan.

## Kalibrasi (kalau ada yang meleset)

- **Atur tombol Next**: saat popup level selesai tampil, tekan tombol ini lalu ketuk posisi tombol Next/Lanjut.
- **Simpan debug.png**: centang, jalankan Auto Play sebentar, lalu lihat
  `Android/data/com.spaceman.vmloader/files/debug.png`. Kotak hijau = tile bebas, merah = tile terblokir.
- Batas area papan dan kemiripan tile ada di `android_overrides/kotlin/Engine.kt` (`TOP`, `BOT`, `THR`).

## Batasan

- Butuh Android 11+ (screenshot lewat layanan aksesibilitas).
- Tile bunga/musim yang beda gambar tapi bisa dipasangkan belum didukung.
