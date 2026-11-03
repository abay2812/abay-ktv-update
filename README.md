# ABAY KTV ROOM - Server Update

Repo ini adalah **tempat update otomatis** untuk aplikasi ABAY KTV ROOM.
Aplikasi di PC pengguna membaca `version.json` di sini untuk mengetahui apakah ada versi baru.

## Alamat yang dipakai aplikasi

| Fungsi | URL |
|---|---|
| Cek versi terbaru | https://raw.githubusercontent.com/abay2812/abay-ktv-update/main/version.json |
| Daftar rilis | https://github.com/abay2812/abay-ktv-update/releases |

## Isi version.json

| Kolom | Arti |
|---|---|
| `versi` | Nomor versi terbaru, misal `1.1.0` |
| `tanggal` | Tanggal rilis |
| `catatan` | Teks yang tampil di banner notifikasi update |
| `url` | Link unduh file zip update |
| `wajib` | `true` jika pengguna harus update (tombol "Nanti" disembunyikan) |

## Cara merilis versi baru

**Langkah 1.** Jalankan `node src/build.js` di PC pembuat, lalu zip isi folder `app/` (tanpa `src/` dan tanpa `lagu_offline/`).

**Langkah 2.** Buka tab **Releases** lalu klik **Draft a new release**. Buat tag baru, misal `v1.1.0`, lalu upload file zip-nya dan klik **Publish release**.

**Langkah 3.** Edit `version.json` di repo ini: naikkan `versi`, isi `catatan`, dan ganti `url` dengan link zip dari rilis tersebut.

Setelah `version.json` disimpan, semua pengguna akan melihat notifikasi update saat membuka aplikasi.

> Catatan: rilis v1.0.0 di repo ini hanya contoh (dummy) untuk menguji alur update.
