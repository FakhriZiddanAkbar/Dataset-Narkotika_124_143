<<<<<<< HEAD
# ⚖️ Dataset Putusan Narkotika dan Psikotropika

**Pengadilan Negeri Kuala Kurun · Tahun Perkara 2023–2025**  
Repository: `Dataset-Narkotika_124_143`

Repository ini memuat dataset dokumen putusan pengadilan beserta metadata pendukung untuk tugas **Ujian Tengah Semester (UTS) mata kuliah Information Retrieval (Temu Kembali Informasi)**, khususnya **SUBCPMK-2: akuisisi dan pengelolaan dokumen putusan pengadilan**. Proyek berfokus pada akuisisi dokumen hukum, pengelolaan metadata, dan dokumentasi dataset sebagai dasar kegiatan temu kembali informasi.

Dataset mencakup **50 dokumen PDF** yang tersedia pada folder hasil ekstraksi dan **50 entri metadata** pada Excel. Dokumen berasal dari Pengadilan Negeri Kuala Kurun, kategori **Pidana Khusus**, dengan klasifikasi **Narkotika dan Psikotropika**.

> **Catatan pemeriksaan:** `Dataset/Narkotika.zip` belum dapat dibaca dengan pembaca ZIP standar. Jumlah 50 PDF telah dikonfirmasi pada folder hasil ekstraksi; keterbacaan dan keutuhan isi arsip ZIP belum terverifikasi. Rincian tersedia pada bagian [Status Pemeriksaan dan Keterbatasan](#status-pemeriksaan-dan-keterbatasan).

## Daftar Isi

- [Anggota Kelompok](#anggota-kelompok)
- [Latar Belakang dan Tujuan](#latar-belakang-dan-tujuan)
- [Sumber dan Metode Pengumpulan](#sumber-dan-metode-pengumpulan)
- [Informasi Dataset](#informasi-dataset)
- [Struktur Direktori](#struktur-direktori)
- [Metadata pada Overview.xlsx](#metadata-pada-overviewxlsx)
- [Cara Mengakses dan Menggunakan Dataset](#cara-mengakses-dan-menggunakan-dataset)
- [Status Pemeriksaan dan Keterbatasan](#status-pemeriksaan-dan-keterbatasan)
- [Referensi Sumber Resmi](#referensi-sumber-resmi)

## Anggota Kelompok

| No. | Nama | Nomor Induk Mahasiswa (NIM) |
| :---: | --- | --- |
| 1 | Rizqullah Zuhayr Alfito Khan | 202310370311124 |
| 2 | Fakhri Ziddan Akbar | 202310370311143 |

## Latar Belakang dan Tujuan

Putusan pengadilan merupakan dokumen hukum yang memuat informasi perkara, barang bukti, pertimbangan, dan amar putusan. Dokumen tersebut dapat digunakan sebagai korpus pembelajaran Information Retrieval untuk mempelajari pencarian informasi pada teks hukum. Pengelolaan dokumen dan metadata yang terstruktur diperlukan agar setiap dokumen dapat dikenali, ditelusuri, dan digunakan kembali secara konsisten.

Penyusunan dataset ini bertujuan untuk:

1. Menghimpun dokumen putusan sesuai cakupan pengadilan, klasifikasi, dan tahun perkara yang ditentukan.
2. Mengorganisasikan dokumen PDF dan metadata perkara dalam repository yang mudah diakses.
3. Menyediakan identitas perkara, informasi barang bukti, dan amar putusan sebagai dasar penelusuran dokumen.
4. Mendokumentasikan sumber, struktur penyimpanan, serta hasil pemeriksaan dan keterbatasan dataset.
5. Menyiapkan bahan untuk pengembangan tahap prapemrosesan teks, pengindeksan, dan pencarian dokumen pada pembelajaran berikutnya.

## Sumber dan Metode Pengumpulan

Sesuai informasi proyek, sumber dokumen adalah **[Direktori Putusan Mahkamah Agung Republik Indonesia](https://putusan3.mahkamahagung.go.id/)**. Portal resmi tersebut menyediakan penelusuran putusan, termasuk [klasifikasi Narkotika dan Psikotropika](https://putusan3.mahkamahagung.go.id/direktori/index/kategori/narkotika-dan-psikotropika-1.html).

Cakupan akuisisi dan bentuk pengelolaan yang didokumentasikan dalam proyek ini meliputi:

| Tahap | Cakupan dan hasil yang tersedia |
| --- | --- |
| Penentuan cakupan | Pengadilan Negeri Kuala Kurun; Pidana Khusus; Narkotika dan Psikotropika; tahun perkara 2023–2025. |
| Akuisisi dokumen | Dokumen putusan tersedia dalam format PDF pada folder hasil ekstraksi. |
| Pengelolaan metadata | Identitas perkara, barang bukti, dan amar putusan dicatat dalam lima kolom pada `Overview/Overview.xlsx`. |
| Penyimpanan | Repository menyediakan `Dataset/Narkotika.zip` dan berkas metadata Excel. ZIP masih memerlukan pemeriksaan lanjutan karena gagal dibaca. |
| Pemeriksaan dokumentasi | Jumlah baris Excel, jumlah PDF lokal, kesesuaian nomor perkara dengan nama berkas, dan keterbacaan arsip diperiksa tanpa mengubah sumber data. |

**Batas dokumentasi metode:** lima kolom Excel tidak mencatat URL sumber setiap putusan, tanggal unduh, maupun alat atau teknik pengunduhan. Oleh karena itu, metode manual atau otomatis dan waktu akuisisi tidak dapat dipastikan dari metadata yang tersedia. Tanggal pada nama berkas tidak diperlakukan sebagai tanggal unduh yang telah terverifikasi.

## Informasi Dataset

| Atribut | Keterangan |
| --- | --- |
| Nama repository | `Dataset-Narkotika_124_143` |
| Pengadilan | Pengadilan Negeri Kuala Kurun (`PN Kuala Kurun`) |
| Kategori | Pidana Khusus |
| Klasifikasi proyek | Narkotika dan Psikotropika |
| Rentang tahun perkara | 2023–2025, berdasarkan tahun pada nomor putusan |
| Jumlah PDF yang terhitung | 50 berkas pada folder hasil ekstraksi |
| Jumlah data Excel | 50 baris data, tidak termasuk satu baris judul kolom |
| Lembar kerja | `Overview` |
| Format dokumen | `.pdf` |
| Format arsip | `.zip` — gagal dibaca pada pemeriksaan saat ini |
| Format metadata | `.xlsx` |
| Bahasa | Bahasa Indonesia |
| Sumber | Direktori Putusan Mahkamah Agung Republik Indonesia |

Distribusi berikut dihitung dari nomor putusan pada Excel dan tahun perkara pada nama PDF di folder hasil ekstraksi:

| Tahun perkara | Entri Excel | PDF hasil ekstraksi |
| :---: | ---: | ---: |
| 2023 | 5 | 5 |
| 2024 | 26 | 26 |
| 2025 | 19 | 19 |
| **Total** | **50** | **50** |

Tahun perkara pada tabel bukan hasil verifikasi tanggal putus atau tanggal unggah. Klasifikasi seluruh dokumen juga belum diperiksa satu per satu terhadap halaman sumber resminya.

## Struktur Direktori

Struktur berkas utama repository:

```text
Dataset-Narkotika_124_143/
├── Dataset/
│   └── Narkotika.zip
├── Overview/
│   └── Overview.xlsx
└── README.md
```

| Lokasi | Fungsi |
| --- | --- |
| [`Dataset/Narkotika.zip`](Dataset/Narkotika.zip) | Arsip dataset; keterbacaan isinya masih bermasalah pada pemeriksaan saat ini. |
| [`Overview/Overview.xlsx`](Overview/Overview.xlsx) | Metadata untuk menelusuri 50 perkara. |
| [`README.md`](README.md) | Dokumentasi proyek, akses dataset, dan hasil pemeriksaan. |

**Folder tambahan yang tersedia secara lokal:** `Dataset/Putusan Pengadilan Negeri Kuala Kurun/` berisi 50 PDF hasil ekstraksi. Folder tersebut berada di luar ringkasan berkas utama di atas dan tetap dipertahankan tanpa penghapusan atau modifikasi. Ketersediaannya pada salinan GitHub perlu diperiksa sebelum digunakan sebagai alternatif akses.

## Metadata pada Overview.xlsx

Berkas [`Overview/Overview.xlsx`](Overview/Overview.xlsx) memiliki satu lembar kerja bernama **`Overview`**, dengan lima kolom berikut. Nama kolom dipertahankan sesuai berkas asli.

| Kolom | Nama kolom | Penjelasan |
| :---: | --- | --- |
| A | `No` | Nomor urut entri dataset, dari 1 sampai 50. Nomor ini bukan nomor perkara. |
| B | `No Putusan` | Identitas perkara, misalnya `1/Pid.Sus/2024/PN Kkn`, untuk mencocokkan metadata dengan dokumen PDF. |
| C | `Lembaga Peradilan` | Nama pengadilan yang menangani perkara. Seluruh entri berisi `PN Kuala Kurun`. |
| D | `Barang Bukti` | Teks mengenai barang bukti yang dicantumkan dalam putusan. Sebagian sel masih memuat fragmen teks di luar bagian barang bukti. |
| E | `Amar Putusan` | Teks bagian amar putusan. Sebagian sel masih memuat disclaimer, penanda halaman, atau fragmen teks lain sehingga perlu dibandingkan dengan PDF saat digunakan. |

Kelima kolom terisi pada seluruh baris data. Keterisian sel tidak menjamin ketepatan, kelengkapan kutipan, atau kebersihan teks. Excel tidak memiliki kolom tersendiri untuk status BHT, URL sumber, atau tanggal akuisisi.

## Cara Mengakses dan Menggunakan Dataset

1. **Unduh repository** melalui **Code → Download ZIP** di GitHub, lalu ekstrak salinan repository ke perangkat lokal. Arsip unduhan repository berbeda dari `Dataset/Narkotika.zip` di dalamnya.
2. **Buka metadata** melalui `Overview/Overview.xlsx` menggunakan Microsoft Excel, LibreOffice Calc, atau aplikasi pembaca `.xlsx` yang sesuai. Gunakan lembar `Overview` untuk menelusuri nomor putusan, barang bukti, dan amar putusan.
3. **Akses dokumen PDF.** Dalam kondisi normal, `Dataset/Narkotika.zip` perlu diekstrak untuk memperoleh PDF. Pada versi yang diperiksa, arsip tersebut gagal dibaca. Jika folder `Dataset/Putusan Pengadilan Negeri Kuala Kurun/` tersedia pada salinan lokal, gunakan PDF di folder itu sebagai alternatif. Jika tidak tersedia, telusuri kembali nomor putusan melalui sumber resmi.
4. **Cocokkan nomor perkara dengan nama PDF.** Contoh pasangan yang tersedia:

   ```text
   No Putusan : 1/Pid.Sus/2024/PN Kkn
   Nama PDF   : putusan_1_pid.sus_2024_pn_kkn_20261104145741.pdf
   ```

   Pencocokan menggunakan nomor, jenis, tahun perkara, dan kode pengadilan; nomor urut pada kolom `No` tidak digunakan sebagai nama berkas.

5. **Gunakan salinan kerja untuk analisis.** Dataset dapat menjadi bahan pencarian kata kunci, ekstraksi teks, prapemrosesan, dan pengindeksan. Bersihkan fragmen watermark atau disclaimer pada salinan turunan, lalu bandingkan informasi penting dengan PDF asli. Simpan hasil pengolahan secara terpisah agar dokumen sumber tetap terjaga.

## Status Pemeriksaan dan Keterbatasan

Pemeriksaan berikut dilakukan pada **10 November 2026** terhadap berkas lokal, dengan akses baca tanpa perubahan pada PDF, Excel, arsip, maupun folder dataset.

| Aspek | Hasil pemeriksaan |
| --- | --- |
| Jumlah dan struktur Excel | Terdapat 50 baris data dan lima kolom pada lembar `Overview`; nomor urut 1–50 lengkap. |
| Keterisian metadata | Tidak ditemukan sel kosong pada kelima kolom untuk 50 baris data. |
| Duplikasi nomor putusan | Tidak ditemukan nomor putusan yang berulang pada Excel. |
| PDF hasil ekstraksi | Terdapat 50 berkas; semuanya memiliki header `%PDF-1.4` dan tidak berukuran kosong. Pemeriksaan ini belum memastikan seluruh halaman dapat dibuka atau seluruh teks dapat diekstrak. |
| Kesesuaian Excel–PDF lokal | Seluruh 50 nomor putusan cocok dengan identitas perkara pada nama PDF hasil ekstraksi. |
| Duplikasi berkas PDF lokal | Tidak ditemukan PDF dengan isi biner identik berdasarkan perbandingan SHA-256. |
| Arsip `Narkotika.zip` | Pembaca Python `zipfile` gagal dengan pesan `Bad magic number for central directory`; `tar` gagal dengan pesan `Truncated ZIP file header`. Arsip terindikasi rusak dan belum dapat dinyatakan siap diekstrak. |
| Indikasi jumlah PDF dalam ZIP | Pemindaian biner menemukan 50 nama PDF unik yang sama dengan nama PDF lokal. Ini hanya indikasi nama berkas, bukan hasil pembacaan arsip yang berhasil; jumlah PDF yang utuh dan dapat diekstrak belum terverifikasi. |
| Kebersihan teks metadata | Kata `Disclaimer` ditemukan pada 9 sel `Barang Bukti` dan 40 sel `Amar Putusan`. Terlihat pula fragmen watermark dan penanda halaman pada sebagian teks. |
| Status berkekuatan hukum tetap (BHT) | Belum diverifikasi per putusan dan tidak dicatat dalam lima kolom Excel. Tidak ditarik kesimpulan bahwa seluruh putusan sudah atau belum BHT. |
| Verifikasi substansi | Ketepatan seluruh kutipan barang bukti, amar putusan, klasifikasi, dan isi setiap PDF terhadap sumber resmi belum diperiksa secara menyeluruh. |

Keterbatasan dan tindak lanjut yang perlu diperhatikan:

- **Akses arsip:** ZIP perlu diperiksa dan, jika diperlukan, dibuat ulang dari sumber PDF yang telah divalidasi sebelum dijadikan jalur distribusi utama. Tidak ada perbaikan atau pengemasan ulang yang dilakukan dalam penyusunan dokumentasi ini.
- **Kualitas metadata:** teks tambahan dapat memengaruhi pencarian kata kunci dan pembentukan indeks. Pembersihan serta verifikasi terhadap dokumen asli diperlukan sebelum analisis yang bergantung pada ketepatan kutipan.
- **Keterlacakan sumber:** URL per putusan dan tanggal akuisisi belum tersedia sebagai kolom metadata, sehingga penelusuran ulang bertumpu pada nomor perkara.
- **Cakupan korpus:** dataset terbatas pada 50 perkara dalam cakupan proyek; kelengkapannya terhadap seluruh populasi putusan pengadilan pada 2023–2025 belum diverifikasi.

## Referensi Sumber Resmi

1. [Direktori Putusan Mahkamah Agung Republik Indonesia](https://putusan3.mahkamahagung.go.id/) — sumber dokumen putusan sesuai informasi proyek.
2. [Direktori Putusan: Narkotika dan Psikotropika](https://putusan3.mahkamahagung.go.id/direktori/index/kategori/narkotika-dan-psikotropika-1.html) — rujukan klasifikasi pada portal resmi.
3. [Situs Resmi Pengadilan Negeri Kuala Kurun](https://www.pn-kualakurun.go.id/) — rujukan institusi pengadilan dan akses layanan informasi.

Untuk penggunaan akademis, cantumkan sumber resmi dan nomor putusan yang dirujuk. Saat membutuhkan kepastian informasi perkara atau status BHT, lakukan verifikasi pada layanan resmi yang relevan.
=======
# Dataset-Narkotika_124_143
>>>>>>> 85db3580cca1776bdfd11c8c607eb11100bb6742
