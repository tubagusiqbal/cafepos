# CafePOS versi satu file HTML

Isi folder ini:
- `index.html`  → satu-satunya file yang di-upload ke GitHub/Vercel
- `Code.gs`     → ditempel ke Google Apps Script (backend + database Google Sheets)
- `appsscript.json` → manifest Apps Script (opsional)

## Langkah
1. Apps Script: buat project di https://script.google.com, tempel `Code.gs`.
   Script Properties: isi `ADMIN_INITIAL_PASSWORD` (min. 10 karakter). **Jangan isi `API_KEY`.**
2. Jalankan `setupDatabase`, lalu `seedSampleData` (opsional).
3. Deploy → New deployment → Web app → Execute as: Me, Access: Anyone → salin URL `/exec`.
4. Buka `index.html`, ganti `GANTI_DENGAN_URL_WEB_APP_ANDA` (baris `GAS_URL`) dengan URL tadi.
5. Upload `index.html` ke GitHub (repo baru), lalu import ke Vercel (Framework: Other, tanpa pengaturan lain).
6. Pelanggan: `https://alamat-anda.vercel.app/` · Staf: `https://alamat-anda.vercel.app/#/login`
   QR meja: `https://alamat-anda.vercel.app/?meja=5#/menu`
