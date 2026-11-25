RUPA V1.0 - DEPLOY KE VERCEL (Versi Tersambung Supabase)

ISI FILE:
- index.html = aplikasi RUPA yang sudah tersambung Supabase Auth + baca rupa_original_assets asli
- config.js = tempat isi Project URL + anon key (WAJIB diisi sebelum deploy)
- vercel.json = konfigurasi Vercel

LANGKAH DI HP:
1. Buka github.com > + > New repository > Nama: rupa-v1 > Create
2. Di repo itu > Add file > Upload files > Upload 3 file ini (index.html, config.js, vercel.json)
   - Sebelum upload, buka config.js di HP, ganti PASTE_URL_DISINI dan PASTE_ANON_KEY_DISINI dengan kunci kamu, lalu simpan.
   - JANGAN upload file yang masih berisi PASTE_..., nanti login gagal.
3. Buka vercel.com > Add New > Project > Import rupa-v1 dari GitHub > Deploy
   - Tidak perlu isi Environment Variables untuk versi ini, karena kunci sudah di config.js.
   - Untuk versi berikutnya, kita pindahkan kunci ke Environment Variables agar lebih aman.
4. Buka domain Vercel di HP > Login pakai email adminsiapgas@rupa.id + password yang kamu buat di Supabase.
   - Kalau berhasil, Home akan tampil nama + ROLE: ADMIN + daftar Silver Collection, Dark Edition, Wallpaper Modern dari database asli.
   - Kalau gagal, pesan error akan muncul di bawah tombol Login — screenshot ke saya.

KEAMANAN:
- config.js hanya berisi anon public key (aman untuk frontend).
- JANGAN pernah taruh service_role key di file ini.
- Untuk production penuh, kita akan ganti config.js menjadi Environment Variables Vercel.
