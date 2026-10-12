ATELIER — GITHUB PAGES + FIREBASE SYNC

FILE UTAMA: atelier_private_art_studio.html
RULES: firestore.rules

PASANG DI GITHUB PAGES
1. Download dan ekstrak ZIP ini.
2. Di repository GitHub yang dipakai untuk GitHub Pages, buka file HTML utama yang sekarang dipakai.
3. Ganti ISI file HTML lama dengan file atelier_private_art_studio.html dari paket ini. Pertahankan nama file/path yang dipakai situs (misalnya index.html jika itu file entrypoint situs).
4. Commit perubahan dan tunggu GitHub Pages selesai deploy. Buka link github.io dan refresh paksa / hapus cache situs bila masih melihat versi lama.
5. Firebase Console → Authentication → Settings → Authorized domains: pastikan hostname GitHub Pages lu tercantum (misalnya USER.github.io, tanpa https/path).
6. Firebase Console → Firestore Database → Rules: publish isi firestore.rules dari paket ini. Rules membatasi data ke UID pemilik akun.
7. Login di perangkat lama terlebih dahulu dan pastikan status menunjukkan cloud tersinkron. Baru buka situs versi baru di perangkat kedua dan login dengan akun yang sama.

PENTING
- Jangan pilih “Lanjutkan tanpa login”; mode itu hanya lokal dan tidak sinkron.
- Jangan hapus data browser lama sebelum proyek berhasil muncul di cloud.
- Paket ini memecah workspace ke dokumen-dokumen kecil agar setiap dokumen tetap di bawah batas Firestore.
- Jika data belum pernah tersimpan ke cloud dari perangkat lama, proyek yang hanya ada di localStorage browser lama tidak otomatis bisa dibaca perangkat lain. Buka versi baru di browser lama dengan data aslinya masih ada agar bisa diunggah.
- Jangan ubah rules menjadi public.
