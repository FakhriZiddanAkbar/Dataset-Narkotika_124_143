# ⚖️ Dataset Putusan Narkotika dan Psikotropika

**Pengadilan Negeri Kuala Kurun · Pidana Khusus · Tahun Perkara 2023–2025**  
Repository: `Dataset-Narkotika_124_143`

Repository ini memuat dataset dokumen putusan pengadilan beserta metadata pendukung untuk tugas **Ujian Tengah Semester (UTS) mata kuliah Temu Kembali Informasi (Information Retrieval)**, Semester Ganjil 2026/2027, khususnya **SUBCPMK-2: memahami metadata, format dokumen, dan markup language dalam Temu Kembali Informasi** melalui akuisisi dan pengelolaan dokumen putusan pengadilan.

Dataset mencakup **50 dokumen putusan berformat PDF** (dikemas dalam `Dataset/Narkotika.zip`) dan **50 entri metadata** pada `Overview/Overview.xlsx`. Seluruh dokumen berasal dari Pengadilan Negeri Kuala Kurun, kategori **Pidana Khusus**, klasifikasi **Narkotika dan Psikotropika**.

## Daftar Isi

- [Anggota Kelompok](#anggota-kelompok)
- [Latar Belakang dan Tujuan](#latar-belakang-dan-tujuan)
- [Sumber dan Cakupan Dataset](#sumber-dan-cakupan-dataset)
- [Informasi Dataset](#informasi-dataset)
- [Struktur Direktori](#struktur-direktori)
- [Metadata pada Overview.xlsx](#metadata-pada-overviewxlsx)
- [Cara Mengakses dan Menggunakan Dataset](#cara-mengakses-dan-menggunakan-dataset)
- [Pengelolaan Kualitas Data](#pengelolaan-kualitas-data)
- [Status Pemeriksaan dan Keterbatasan](#status-pemeriksaan-dan-keterbatasan)
- [Referensi Sumber Resmi](#referensi-sumber-resmi)

## Anggota Kelompok

| No. | Nama | Nomor Induk Mahasiswa (NIM) |
| :---: | --- | --- |
| 1 | Rizqullah Zuhayr Alfito Khan | 202310370311124 |
| 2 | Fakhri Ziddan Akbar | 202310370311143 |

## Latar Belakang dan Tujuan

Putusan pengadilan merupakan dokumen hukum yang memuat identitas perkara, barang bukti, pertimbangan hakim, dan amar putusan. Sifatnya yang terbuka menjadikan putusan sumber pengetahuan sekaligus korpus yang layak untuk pembelajaran Information Retrieval pada teks hukum. Agar dapat dikenali, ditelusuri, dan digunakan kembali, dokumen perlu dikelola bersama metadata yang terstruktur.

Penyusunan dataset ini bertujuan untuk:

1. Menghimpun dokumen putusan sesuai cakupan pengadilan, klasifikasi, dan tahun perkara yang ditentukan.
2. Mengorganisasikan dokumen PDF dan metadata perkara dalam repository publik yang mudah diakses.
3. Menyediakan identitas perkara, barang bukti, dan amar putusan sebagai dasar penelusuran dokumen.
4. Mendokumentasikan sumber, struktur penyimpanan, pengelolaan kualitas data, serta keterbatasan dataset.
5. Menyiapkan bahan untuk tahap lanjutan: crawling, prapemrosesan teks, pengindeksan, dan pencarian dokumen.

## Sumber dan Cakupan Dataset

Sumber dokumen adalah **[Direktori Putusan Mahkamah Agung Republik Indonesia](https://putusan3.mahkamahagung.go.id/direktori.html)**, termasuk [klasifikasi Narkotika dan Psikotropika](https://putusan3.mahkamahagung.go.id/direktori/index/kategori/narkotika-dan-psikotropika-1.html).

| Parameter | Nilai |
| --- | --- |
| Pengadilan | Pengadilan Negeri Kuala Kurun (`PN Kuala Kurun`) |
| Kategori | Pidana Khusus (`Pid.Sus`) |
| Klasifikasi | Narkotika dan Psikotropika |
| Tahun perkara | 2023–2025 |
| Jumlah putusan | 50 |

**Batas dokumentasi metode:** lima kolom pada Excel tidak mencatat URL sumber tiap putusan maupun tanggal unduh. Angka pada akhir nama berkas PDF (misalnya `20261104145741`) hanya bagian dari nama berkas dan tidak diperlakukan sebagai tanggal unduh yang terverifikasi.

## Informasi Dataset

| Atribut | Keterangan |
| --- | --- |
| Nama repository | `Dataset-Narkotika_124_143` |
| Pengadilan | Pengadilan Negeri Kuala Kurun |
| Kategori / klasifikasi | Pidana Khusus / Narkotika dan Psikotropika |
| Rentang tahun perkara | 2023–2025, berdasarkan tahun pada nomor putusan |
| Jumlah dokumen | 50 PDF di dalam `Dataset/Narkotika.zip` |
| Jumlah data metadata | 50 baris data (di luar satu baris judul kolom) |
| Lembar kerja | `Overview` |
| Format dokumen | `.pdf` (dalam arsip `.zip`) |
| Format metadata | `.xlsx` |
| Bahasa | Bahasa Indonesia |

Distribusi tahun perkara, dihitung dari nomor putusan:

| Tahun perkara | Jumlah putusan |
| :---: | ---: |
| 2023 | 5 |
| 2024 | 26 |
| 2025 | 19 |
| **Total** | **50** |

## Struktur Direktori

```text
Dataset-Narkotika_124_143/
├── Dataset/
│   └── Narkotika.zip        # arsip berisi 50 PDF putusan (folder Narkotika/)
├── Overview/
│   └── Overview.xlsx        # ringkasan 50 putusan (5 kolom)
└── README.md
```

| Lokasi | Fungsi |
| --- | --- |
| [`Dataset/Narkotika.zip`](Dataset/Narkotika.zip) | Arsip dataset: 50 dokumen putusan berekstensi `.pdf` dalam folder `Narkotika/`. |
| [`Overview/Overview.xlsx`](Overview/Overview.xlsx) | Metadata dan ringkasan 50 putusan. |
| [`README.md`](README.md) | Dokumentasi dataset. |

## Metadata pada Overview.xlsx

Berkas memiliki satu lembar kerja bernama **`Overview`** dengan lima kolom:

| Kolom | Nama kolom | Penjelasan |
| :---: | --- | --- |
| A | `No` | Nomor urut entri dataset, 1 sampai 50. Bukan nomor perkara. |
| B | `No Putusan` | Nomor perkara, misalnya `102/Pid.Sus/2024/PN Kkn`. |
| C | `Lembaga Peradilan` | Pengadilan yang menangani perkara; seluruh entri berisi `PN Kuala Kurun`. |
| D | `Barang Bukti` | Daftar barang bukti yang ditetapkan dalam amar putusan. |
| E | `Amar Putusan` | Teks amar putusan, mulai dari butir pertama setelah kata *MENGADILI* hingga butir terakhir (biaya perkara). |

Kelima kolom terisi pada seluruh baris. Setiap nomor putusan pada kolom B bersesuaian satu-satu dengan satu berkas PDF di dalam arsip, dengan pola nama `putusan_<nomor>_pid.sus_<tahun>_pn_kkn_<angka>.pdf`.

Contoh pasangan:

```text
No Putusan : 1/Pid.Sus/2024/PN Kkn
Nama PDF   : putusan_1_pid.sus_2024_pn_kkn_20261104145741.pdf
```

## Cara Mengakses dan Menggunakan Dataset

1. **Unduh repository** melalui **Code → Download ZIP**, atau lakukan `git clone`.
2. **Ekstrak dokumen**: ekstrak `Dataset/Narkotika.zip` untuk memperoleh folder `Narkotika/` berisi 50 PDF.

   ```bash
   unzip Dataset/Narkotika.zip -d Dataset/
   ```

3. **Buka metadata** `Overview/Overview.xlsx` dengan Microsoft Excel, LibreOffice Calc, atau pustaka seperti `pandas`:

   ```python
   import pandas as pd
   df = pd.read_excel("Overview/Overview.xlsx", sheet_name="Overview")
   print(df.shape)  # (50, 5)
   ```

4. **Cocokkan metadata dengan dokumen** menggunakan nomor, jenis, tahun perkara, dan kode pengadilan pada nama berkas; kolom `No` tidak digunakan sebagai nama berkas.
5. **Gunakan salinan kerja** untuk prapemrosesan dan pengindeksan, dan simpan hasil olahan terpisah dari dokumen sumber.

## Pengelolaan Kualitas Data

Teks hasil ekstraksi langsung dari PDF Direktori Putusan memuat gangguan berupa watermark diagonal ("Direktori Putusan Mahkamah Agung Republik Indonesia"), blok *Disclaimer* Kepaniteraan Mahkamah Agung, serta penanda halaman. Gangguan ini memecah kata dan menyisipkan huruf lepas pada kolom `Barang Bukti` dan `Amar Putusan`, sehingga merugikan pencarian kata kunci dan pembentukan indeks.

Pada versi ini, kedua kolom tersebut disusun ulang dari teks PDF dengan tahapan berikut:

1. Karakter lapisan watermark dan catatan kaki (font `Helvetica`) disaring, sedangkan teks isi putusan (font `LiberationSans`/`LiberationSerif`) dipertahankan.
2. Baris penanda halaman (`Halaman n dari m Putusan Nomor ...`) dihapus dan spasi dirapikan.
3. **Amar Putusan** diambil dari butir pertama setelah kata *MENGADILI* (dalam bentuk apa pun, termasuk `M E N G A D I L I`) sampai sebelum kalimat *Demikianlah diputuskan ...*.
4. **Barang Bukti** diambil dari butir amar *Menetapkan barang bukti berupa* sampai sebelum butir berikutnya (umumnya *Membebankan biaya perkara*).
5. Hasil diperiksa otomatis: tidak ada sel yang kosong dan tidak tersisa kata *Disclaimer*, *Kepaniteraan*, alamat situs Mahkamah Agung, maupun penanda halaman pada kedua kolom.

Kolom `No`, `No Putusan`, dan `Lembaga Peradilan` tidak diubah.

## Status Pemeriksaan dan Keterbatasan

Pemeriksaan dilakukan pada **11 November 2026**.

| Aspek | Hasil pemeriksaan |
| --- | --- |
| Struktur Excel | 50 baris data dan lima kolom pada lembar `Overview`; nomor urut 1–50 lengkap. |
| Keterisian metadata | Tidak ada sel kosong pada kelima kolom. |
| Duplikasi nomor putusan | Tidak ada nomor putusan yang berulang. |
| Arsip `Narkotika.zip` | Dapat dibaca dan lolos uji integritas (`testzip`); berisi 50 berkas PDF yang isinya identik dengan PDF sumber berdasarkan perbandingan SHA-256. |
| Kesesuaian Excel–PDF | Seluruh 50 nomor putusan cocok dengan 50 nama PDF di dalam arsip. |
| Keterbacaan teks PDF | Teks dapat diekstrak dari seluruh 50 PDF. |
| Kebersihan teks metadata | Lihat bagian [Pengelolaan Kualitas Data](#pengelolaan-kualitas-data). |
| Status berkekuatan hukum tetap (BHT) | Tidak tercatat dalam metadata dan tidak dapat disimpulkan dari isi PDF; status per putusan perlu dicek pada halaman putusan di Direktori Putusan. |

Keterbatasan yang perlu diperhatikan:

- **Segmentasi otomatis:** kolom `Barang Bukti` dan `Amar Putusan` dibentuk dengan pola teks sehingga format penulisan yang tidak lazim pada putusan tertentu dapat menggeser batas kutipan. Untuk analisis yang bergantung pada ketepatan kutipan, bandingkan dengan PDF asli.
- **Keterlacakan sumber:** URL per putusan dan tanggal akuisisi belum tersedia sebagai kolom metadata, sehingga penelusuran ulang bertumpu pada nomor perkara.
- **Cakupan korpus:** dataset terbatas pada 50 perkara sesuai cakupan tugas; kelengkapannya terhadap seluruh putusan PN Kuala Kurun pada 2023–2025 tidak diverifikasi.

## Referensi Sumber Resmi

1. [Direktori Putusan Mahkamah Agung Republik Indonesia](https://putusan3.mahkamahagung.go.id/direktori.html): sumber dokumen putusan.
2. [Direktori Putusan: Narkotika dan Psikotropika](https://putusan3.mahkamahagung.go.id/direktori/index/kategori/narkotika-dan-psikotropika-1.html): rujukan klasifikasi.
3. [Situs Resmi Pengadilan Negeri Kuala Kurun](https://www.pn-kualakurun.go.id/): rujukan institusi pengadilan.

Untuk penggunaan akademis, cantumkan sumber resmi dan nomor putusan yang dirujuk. Untuk kepastian informasi perkara atau status BHT, lakukan verifikasi pada layanan resmi yang relevan.