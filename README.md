# Acumalaka Tracker

Acumalaka Tracker adalah expense tracker dengan frontend HTML/CSS/JavaScript dan backend Python Flask. Data anggaran dan transaksi disimpan secara lokal di SQLite.

## Menjalankan aplikasi

1. Pastikan Python 3.10 atau lebih baru sudah terpasang.
2. Buka terminal di folder project, lalu jalankan:

   ```powershell
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1
   pip install -r requirements.txt
   python app.py
   ```

3. Buka <http://127.0.0.1:5000> di browser.

Database dibuat otomatis di `instance/rapi.sqlite3`. Jangan membuka `index.html` langsung dari file; jalankan server agar frontend dapat berkomunikasi dengan backend.

## Riwayat bulanan

Transaksi hanya dapat dicatat pada bulan berjalan. Ketika bulan berganti, transaksi bulan sebelumnya otomatis muncul di menu **Riwayat**. Anggaran bulan baru mengikuti anggaran bulan terakhir sampai pengguna mengubahnya. Pilih arsip bulan untuk melihat total, rincian kategori, dan transaksi, lalu gunakan **Cetak riwayat** untuk mencetak atau menyimpan sebagai PDF dari dialog cetak browser.

## Menjalankan tes

```powershell
python -m unittest discover -s tests
```
