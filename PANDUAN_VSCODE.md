# Menjalankan notebook di VS Code

1. Pastikan Python, VS Code, serta ekstensi **Python** dan **Jupyter** dari Microsoft sudah terpasang.
2. Di VS Code, pilih **File → Open Folder**, lalu buka folder `Dataset-Narkotika_124_143` ini.
3. Buka terminal VS Code dan jalankan:

   ```powershell
   python -m venv .venv
   .\.venv\Scripts\python.exe -m pip install ipykernel pymupdf pandas requests beautifulsoup4 lxml
   ```

4. Buka `SUBCPMK_3_PN_Kuala_Kurun_CRAWLER_ALTERNATIF_REVISI.ipynb`.
5. Klik **Select Kernel → Python Environments**, lalu pilih Python di `.venv`. Jika belum muncul, gunakan **Python: Select Interpreter** dari Command Palette dan pilih `.venv\Scripts\python.exe`, kemudian pilih kernel kembali.
6. Klik **Run All**, atau jalankan sel berurutan dari atas ke bawah. Sel instalasi menggunakan `%pip` agar pustaka terpasang pada Python milik kernel. Instalasi pustaka membutuhkan internet.

Input bawaan adalah `Dataset/Putusan Pengadilan Negeri Kuala Kurun/Narkotika_Baru.zip`, yang berisi 50 PDF dan sudah diperiksa keutuhan ZIP-nya. Arsip lama `Dataset/Narkotika.zip` rusak. Untuk memakai ZIP PDF/TXT lain, ubah `ZIP_PATH` di bagian 2. File sumber tetap dipertahankan.

Hasil PDF, TXT, CSV, laporan, serta ZIP TXT tersimpan di `SUBCPMK3_REVISI/`; hasil akhir berada di `SUBCPMK3_REVISI/Output/`. Tidak perlu tombol unduh Colab karena hasil sudah ada di komputer.

Bagian crawler membutuhkan internet dan tetap mengikuti pemeriksaan `robots.txt` serta batas akses pada kode asli. Jika akses ditolak atau jaringan gagal, laporan akses tetap dibuat; hasil metadata bisa kosong.

Untuk HTML manual opsional, simpan halaman publik dari browser, ubah `UPLOAD_HTML_MANUAL = True`, lalu isi `MANUAL_HTML_PATHS`, misalnya `[PROJECT_DIR / 'halaman_putusan.html']`. Biarkan `False` jika tidak memakai HTML manual.

Logika ekstraksi, pembersihan teks, validasi, pencocokan, aturan crawler, dan format CSV dipertahankan. Penyesuaian mencakup instalasi pada kernel, lokasi input/output lokal, pengganti unggah/unduh Colab, serta perbaikan `WORK` yang belum didefinisikan menjadi `ROOT` pada lokasi HTML.
