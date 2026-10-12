ATELIER — PRIVATE ART STUDIO
Workspace pribadi per akun + sinkronisasi Firestore

Isi:
- atelier_private_art_studio.html: HTML Atelier dengan pemisahan workspace berdasarkan UID akun Firebase.
- firestore.rules: Rules Firestore yang membatasi tiap akun ke dokumen users/{uid}/workspace/{workspaceId} miliknya.

Cara pakai:
1. Di Firebase Console > Authentication > Sign-in method, aktifkan Email/Password (dan Google bila ingin dipakai).
2. Pastikan Firebase project pada HTML sesuai dengan project milikmu (project ID saat ini: a-draw).
3. Di Firestore > Rules, pasang isi file firestore.rules lalu tekan Publish.
4. Buka HTML melalui HTTPS/host yang diizinkan Firebase; login atau buat akun.
5. Setiap UID mendapat dokumen users/{UID}/workspace/atelier. Login akun yang sama di perangkat lain untuk mengambil workspace yang sama; akun berbeda mendapat workspace terpisah.

Penting:
- Sinkronisasi harus diuji dengan akun nyata; paket ini tidak dapat menguji koneksi ke project Firebase milikmu dari sini.
- Versi ini memisahkan data workspace utama (proyek, referensi, karakter, jurnal, palet, profil) per akun. Fitur tambahan yang menyimpan data langsung ke localStorage dengan kunci terpisah, seperti galeri pose/anatomi pribadi, mungkin masih hanya tersimpan di perangkat dan belum tersinkron.
- Data lama pada kunci lokal lama akan dimigrasikan sekali ke akun pertama yang masuk pada browser ini jika akun itu belum memiliki workspace cloud. Periksa data setelah login pertama.
- Jangan mengganti Rules dengan izin baca/tulis publik.
