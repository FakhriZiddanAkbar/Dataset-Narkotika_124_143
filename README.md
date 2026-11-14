⚖️ Dataset dan Pengolahan Putusan Narkotika dan Psikotropika

Pengadilan Negeri Kuala Kurun · Pidana Khusus · Tahun Perkara 2023–2025
Repository: Dataset-Narkotika_124_143

Repository ini memuat seluruh pekerjaan Ujian Tengah Semester (UTS) Temu Kembali Informasi (Information Retrieval), Semester Ganjil 2026/2027, Kelas A, D. Isinya dataset 50 putusan pengadilan beserta metadata (SUBCPMK-2), hasil ekstraksi dan crawler (SUBCPMK-3), serta preprocessing, pengindeksan, pembobotan, dan mesin pencari (SUBCPMK-4).

Ringkasan Pengerjaan
SUBCPMK	Topik	Keluaran utama di repository
2	Metadata, format dokumen, dan markup language: akuisisi dan pengelolaan dokumen	Dataset/Narkotika.zip (50 PDF), Overview/Overview.xlsx (50 baris, 5 kolom)
3	Ekstraksi PDF → TXT → CSV dan web crawler metadata Direktori Putusan MA	SUBCPMK_3_PN_Kuala_Kurun_FINAL_BUKTI_DIREKTORI.ipynb, folder OUTPUT SUBCPMK 3/
4	Model TKI dan teknik pembobotan dalam pengindeksan dan pencarian teks	UTS_IR_SUBCPMK4_Indexing.ipynb (Colab), folder OUTPUT SUBCPMK 4/
Daftar Isi
Anggota Kelompok
Struktur Repository
SUBCPMK-2: Dataset dan Metadata
SUBCPMK-3: Ekstraksi dan Web Crawler
SUBCPMK-4: Preprocessing, Indexing, dan Pencarian
Cara Menjalankan
Keterbatasan Keseluruhan
Referensi Sumber Resmi
Anggota Kelompok
No.	Nama	Nomor Induk Mahasiswa (NIM)
1	Rizqullah Zuhayr Alfito Khan	202310370311124
2	Fakhri Ziddan Akbar	202310370311143
Struktur Repository
text
Dataset-Narkotika_124_143/
├── Dataset/
│   ├── Narkotika.zip                                   # SUBCPMK-2: 50 PDF putusan (folder Narkotika/)
│   └── Putusan Pengadilan Negeri Kuala Kurun/
│       └── Narkotika_Baru.zip                          # salinan arsip 50 PDF (input bawaan notebook SUBCPMK-3)
├── Overview/
│   └── Overview.xlsx                                   # SUBCPMK-2: metadata 50 putusan
├── SUBCPMK_3_PN_Kuala_Kurun_FINAL_BUKTI_DIREKTORI.ipynb
├── OUTPUT SUBCPMK 3/
│   ├── PDF/                                            # 50 PDF hasil unggah
│   ├── TXT/                                            # 50 TXT hasil konversi
│   └── Output/                                         # CSV, JSON, log, dan ZIP TXT
├── UTS_IR_SUBCPMK4_Indexing.ipynb                      # SUBCPMK-4 (dijalankan di Google Colab)
├── OUTPUT SUBCPMK 4/
│   ├── txt/                                            # 50 teks penuh hasil ekstraksi
│   ├── indeks_putusan.pkl                              # inverted index
│   ├── kamus_term.csv, korpus_praproses.csv, ringkasan_putusan.csv, hasil_evaluasi.csv
│   ├── perbandingan_metode.png, zipf.png
│   └── hasil_subcpmk4.zip                              # paket seluruh keluaran
├── PANDUAN_VSCODE.md                                   # cara menjalankan notebook di VS Code
└── README.md
SUBCPMK-2: Dataset dan Metadata

SUBCPMK-2 menyiapkan korpus: 50 putusan PDF dari Pengadilan Negeri Kuala Kurun (Pidana Khusus, Narkotika dan Psikotropika, tahun 2023–2025) dan 50 baris metadata pada Overview/Overview.xlsx.

2.1 Latar Belakang dan Tujuan

Putusan pengadilan merupakan dokumen hukum yang memuat identitas perkara, barang bukti, pertimbangan hakim, dan amar putusan. Sifatnya yang terbuka menjadikan putusan sumber pengetahuan sekaligus korpus yang layak untuk pembelajaran Information Retrieval pada teks hukum. Agar dapat dikenali, ditelusuri, dan digunakan kembali, dokumen perlu dikelola bersama metadata yang terstruktur.

Penyusunan dataset ini bertujuan untuk:

Menghimpun dokumen putusan sesuai cakupan pengadilan, klasifikasi, dan tahun perkara yang ditentukan.
Mengorganisasikan dokumen PDF dan metadata perkara dalam repository publik yang mudah diakses.
Menyediakan identitas perkara, barang bukti, dan amar putusan sebagai dasar penelusuran dokumen.
Mendokumentasikan sumber, struktur penyimpanan, pengelolaan kualitas data, serta keterbatasan dataset.
Menyiapkan bahan untuk tahap lanjutan: crawling, prapemrosesan teks, pengindeksan, dan pencarian dokumen.
2.2 Sumber dan Cakupan Dataset

Sumber dokumen adalah Direktori Putusan Mahkamah Agung Republik Indonesia, termasuk klasifikasi Narkotika dan Psikotropika.

Parameter	Nilai
Pengadilan	Pengadilan Negeri Kuala Kurun (PN Kuala Kurun)
Kategori	Pidana Khusus (Pid.Sus)
Klasifikasi	Narkotika dan Psikotropika
Tahun perkara	2023–2025
Jumlah putusan	50

Batas dokumentasi metode: lima kolom pada Excel tidak mencatat URL sumber tiap putusan maupun tanggal unduh. Angka pada akhir nama berkas PDF (misalnya 20261104145741) hanya bagian dari nama berkas dan tidak diperlakukan sebagai tanggal unduh yang terverifikasi.

2.3 Informasi Dataset
Atribut	Keterangan
Nama repository	Dataset-Narkotika_124_143
Pengadilan	Pengadilan Negeri Kuala Kurun
Kategori / klasifikasi	Pidana Khusus / Narkotika dan Psikotropika
Rentang tahun perkara	2023–2025, berdasarkan tahun pada nomor putusan
Jumlah dokumen	50 PDF di dalam Dataset/Narkotika.zip
Jumlah data metadata	50 baris data (di luar satu baris judul kolom)
Lembar kerja	Overview
Format dokumen	.pdf (dalam arsip .zip)
Format metadata	.xlsx
Bahasa	Bahasa Indonesia

Distribusi tahun perkara, dihitung dari nomor putusan:

Tahun perkara	Jumlah putusan
2023	5
2024	26
2025	19
Total	50
2.4 Struktur Direktori Dataset Awal
text
Dataset-Narkotika_124_143/
├── Dataset/
│   └── Narkotika.zip        # arsip berisi 50 PDF putusan (folder Narkotika/)
├── Overview/
│   └── Overview.xlsx        # ringkasan 50 putusan (5 kolom)
└── README.md
Lokasi	Fungsi
Dataset/Narkotika.zip	Arsip dataset: 50 dokumen putusan berekstensi .pdf dalam folder Narkotika/.
Overview/Overview.xlsx	Metadata dan ringkasan 50 putusan.
README.md	Dokumentasi dataset.
2.5 Metadata pada Overview.xlsx

Berkas memiliki satu lembar kerja bernama Overview dengan lima kolom:

Kolom	Nama kolom	Penjelasan
A	No	Nomor urut entri dataset, 1 sampai 50. Bukan nomor perkara.
B	No Putusan	Nomor perkara, misalnya 102/Pid.Sus/2024/PN Kkn.
C	Lembaga Peradilan	Pengadilan yang menangani perkara; seluruh entri berisi PN Kuala Kurun.
D	Barang Bukti	Daftar barang bukti yang ditetapkan dalam amar putusan.
E	Amar Putusan	Teks amar putusan, mulai dari butir pertama setelah kata MENGADILI hingga butir terakhir (biaya perkara).

Kelima kolom terisi pada seluruh baris. Setiap nomor putusan pada kolom B bersesuaian satu-satu dengan satu berkas PDF di dalam arsip, dengan pola nama putusan_<nomor>_pid.sus_<tahun>_pn_kkn_<angka>.pdf.

Contoh pasangan:

text
No Putusan : 1/Pid.Sus/2024/PN Kkn
Nama PDF   : putusan_1_pid.sus_2024_pn_kkn_20261104145741.pdf
2.6 Cara Mengakses dan Menggunakan Dataset
Unduh repository melalui Code → Download ZIP, atau lakukan git clone.
Ekstrak dokumen: ekstrak Dataset/Narkotika.zip untuk memperoleh folder Narkotika/ berisi 50 PDF.
bash
unzip Dataset/Narkotika.zip -d Dataset/
Buka metadata Overview/Overview.xlsx dengan Microsoft Excel, LibreOffice Calc, atau pustaka seperti pandas:
python
import pandas as pd
df = pd.read_excel("Overview/Overview.xlsx", sheet_name="Overview")
print(df.shape)  # (50, 5)
Cocokkan metadata dengan dokumen menggunakan nomor, jenis, tahun perkara, dan kode pengadilan pada nama berkas; kolom No tidak digunakan sebagai nama berkas.
Gunakan salinan kerja untuk prapemrosesan dan pengindeksan, dan simpan hasil olahan terpisah dari dokumen sumber.
2.7 Pengelolaan Kualitas Data

Teks hasil ekstraksi langsung dari PDF Direktori Putusan memuat gangguan berupa watermark diagonal ("Direktori Putusan Mahkamah Agung Republik Indonesia"), blok Disclaimer Kepaniteraan Mahkamah Agung, serta penanda halaman. Gangguan ini memecah kata dan menyisipkan huruf lepas pada kolom Barang Bukti dan Amar Putusan, sehingga merugikan pencarian kata kunci dan pembentukan indeks.

Pada versi ini, kedua kolom tersebut disusun ulang dari teks PDF dengan tahapan berikut:

Karakter lapisan watermark dan catatan kaki (font Helvetica) disaring, sedangkan teks isi putusan (font LiberationSans/LiberationSerif) dipertahankan.
Baris penanda halaman (Halaman n dari m Putusan Nomor ...) dihapus dan spasi dirapikan.
Amar Putusan diambil dari butir pertama setelah kata MENGADILI (dalam bentuk apa pun, termasuk M E N G A D I L I) sampai sebelum kalimat Demikianlah diputuskan ....
Barang Bukti diambil dari butir amar Menetapkan barang bukti berupa sampai sebelum butir berikutnya (umumnya Membebankan biaya perkara).
Hasil diperiksa otomatis: tidak ada sel yang kosong dan tidak tersisa kata Disclaimer, Kepaniteraan, alamat situs Mahkamah Agung, maupun penanda halaman pada kedua kolom.

Kolom No, No Putusan, dan Lembaga Peradilan tidak diubah.

2.8 Status Pemeriksaan dan Keterbatasan

Pemeriksaan dilakukan pada 11 November 2026 (SUBCPMK-2).

Aspek	Hasil pemeriksaan
Struktur Excel	50 baris data dan lima kolom pada lembar Overview; nomor urut 1–50 lengkap.
Keterisian metadata	Tidak ada sel kosong pada kelima kolom.
Duplikasi nomor putusan	Tidak ada nomor putusan yang berulang.
Arsip Narkotika.zip	Dapat dibaca dan lolos uji integritas (testzip); berisi 50 berkas PDF yang isinya identik dengan PDF sumber berdasarkan perbandingan SHA-256.
Kesesuaian Excel–PDF	Seluruh 50 nomor putusan cocok dengan 50 nama PDF di dalam arsip.
Keterbacaan teks PDF	Teks dapat diekstrak dari seluruh 50 PDF.
Kebersihan teks metadata	Lihat bagian Pengelolaan Kualitas Data.
Status berkekuatan hukum tetap (BHT)	Tidak tercatat dalam metadata dan tidak dapat disimpulkan dari isi PDF; status per putusan perlu dicek pada halaman putusan di Direktori Putusan.

Keterbatasan yang perlu diperhatikan:

Segmentasi otomatis: kolom Barang Bukti dan Amar Putusan dibentuk dengan pola teks sehingga format penulisan yang tidak lazim pada putusan tertentu dapat menggeser batas kutipan. Untuk analisis yang bergantung pada ketepatan kutipan, bandingkan dengan PDF asli.
Keterlacakan sumber: URL per putusan dan tanggal akuisisi belum tersedia sebagai kolom metadata, sehingga penelusuran ulang bertumpu pada nomor perkara.
Cakupan korpus: dataset terbatas pada 50 perkara sesuai cakupan tugas; kelengkapannya terhadap seluruh putusan PN Kuala Kurun pada 2023–2025 tidak diverifikasi.
SUBCPMK-3: Ekstraksi dan Web Crawler

Notebook: SUBCPMK_3_PN_Kuala_Kurun_FINAL_BUKTI_DIREKTORI.ipynb. Panduan menjalankannya di VS Code ada di PANDUAN_VSCODE.md.

3.1 Alur
Memuat ZIP berisi 50 PDF (input bawaan: Dataset/Putusan Pengadilan Negeri Kuala Kurun/Narkotika_Baru.zip).
Konversi PDF → TXT untuk 50 putusan (OUTPUT SUBCPMK 3/TXT/).
Ekstraksi nomor putusan, lembaga peradilan, barang bukti, dan amar putusan, termasuk pembersihan watermark dan disclaimer Mahkamah Agung.
Pemeriksaan mutu: audit residu watermark dan footer, serta kolom Catatan QA dan Pemeriksaan Manual (seluruh baris bertanda CEK SAMPEL / SUMBER, yaitu perlu dicocokkan sampelnya dengan PDF asli).
Web crawler metadata Direktori Putusan MA: pemeriksaan robots.txt, pembatasan jumlah request, pencatatan status akses, parsing HTML, filter PN Kuala Kurun, lalu pencocokan dengan 50 nomor putusan.
Jalur alternatif: SIPP PN Kuala Kurun, HTML publik yang disimpan manual dari browser, dan parsing arsip halaman daftar putusan (PDF cetakan Chrome) sebagai bukti tambahan.
3.2 Keluaran (OUTPUT SUBCPMK 3/Output/)
Berkas	Isi
hasil_ekstraksi_putusan_BERSIH.csv	50 baris: No, No Putusan, Lembaga Peradilan, Barang Bukti, Amar Putusan
laporan_validasi_BERSIH.csv	Hasil ekstraksi ditambah Nama File, Catatan QA, Pemeriksaan Manual
TXT_50_Putusan.zip	50 berkas TXT hasil konversi
metadata_crawling_PN_Kuala_Kurun.csv	Metadata dari crawler (kosong, lihat 3.3)
pencocokan_crawling_50_putusan.csv	Pencocokan 50 putusan dengan hasil crawler
log_akses_crawling.csv, ringkasan_crawling.json	Bukti akses dan ringkasan crawler
metadata_sumber_alternatif.csv, pencocokan_sumber_alternatif_50_putusan.csv, log_sumber_alternatif.csv, ringkasan_sumber_alternatif.json	Hasil dan bukti jalur alternatif
3.3 Hasil dan penjelasan crawler
Percobaan	Hasil
https://putusan3.mahkamahagung.go.id/direktori.html	HTTP 403, tidak diteruskan
Halaman klasifikasi Narkotika dan Psikotropika	HTTP 403, tidak diteruskan
https://sipp.pn-kualakurun.go.id/robots.txt	HTTP 404: izin tidak dapat diverifikasi, sehingga request halaman dibatalkan
Ringkasan	halaman berhasil diakses: 0, metadata ditemukan: 0, data lokal: 50, data cocok: 0

Karena server Direktori MA menolak akses otomatis, metadata dari situs tidak berhasil dikumpulkan secara langsung. Crawler tetap mematuhi robots.txt dan pembatasan akses, dan semua penolakan dicatat pada log. Metadata tidak dikarang: bila halaman tidak dapat diakses, CSV dibiarkan kosong dan status pencocokan dicatat Tidak ditemukan pada halaman yang diakses. Status itu berarti tidak ditemukan pada halaman yang sempat diakses, bukan berarti putusan tidak ada di Mahkamah Agung. Metode perolehan yang berbeda (crawling HTTP, SIPP, HTML tersimpan, arsip PDF dari Chrome) tidak disamakan satu sama lain.

Data yang sah untuk tahap berikutnya adalah hasil ekstraksi dari 50 PDF (hasil_ekstraksi_putusan_BERSIH.csv).

SUBCPMK-4: Preprocessing, Indexing, dan Pencarian

Notebook: UTS_IR_SUBCPMK4_Indexing.ipynb, dirancang untuk Google Colab dan mengunduh dataset langsung dari repository ini (repository harus Public). Seluruh algoritma indeks dan pembobotan ditulis sendiri.

4.1 Ekstraksi dan segmentasi (seluruh bagian putusan)
Teks diekstrak dengan pdfplumber. Karakter lapisan watermark dan disclaimer MA (font Helvetica) dibuang sebelum teks dibentuk, sehingga kata tidak terpecah oleh huruf lepas.
Tiap putusan dibagi menjadi empat bidang yang saling lepas dan menutup seluruh teks: kepala (identitas dan dakwaan awal), pertimbangan, amar (setelah MENGADILI), dan penutup. Notebook memeriksa bahwa keempatnya menutup teks pada 50 dari 50 dokumen.
Metadata turunan: terdakwa, umur, jenis kelamin, pekerjaan, tuntutan, pidana penjara, denda, dan tanggal putusan, selain barang bukti dan amar. Nomor putusan identik dengan Overview.xlsx.
Ukuran korpus: 50 dokumen, rata-rata ±72.000 karakter per putusan, total ±3,6 juta karakter.
4.2 Preprocessing bertahap
Tahap	Perlakuan	Kosakata (% dari tahap A)
A. Dasar	casefolding dan tokenisasi	100 (5.173 term)
B. + Stopword	stopword Sastrawi ditambah stopword domain putusan	90,7
C. + Normalisasi	angka (Rp1.000.000.000,00 → rp 1000000000) dan varian kata (shabu→sabu, narkoba→narkotika, handphone→hp, als→alias)	90,8
D. + Stemming	stemming Sastrawi dengan cache	69,9 (3.618 term)
4.3 Indexing dan pembobotan

Inverted index dibangun sendiri sebagai matriks sparse dokumen × term (scipy), lengkap dengan frekuensi dan posisi kata (untuk pencarian frasa). Empat skema pembobotan:

Skema	Rumus ringkas
TF mentah	skor = jumlah kemunculan kata kueri
TF-IDF + cosine	(1 + log tf) × idf, idf = log((1+N)/(1+df)) + 1, normalisasi L2, kemiripan kosinus. Divalidasi terhadap TfidfVectorizer scikit-learn: selisih skor maksimum ≈ 1e-16
BM25	k1 = 1,5, b = 0,75, idf = log(1 + (N − df + 0,5)/(df + 0,5))
BM25 berbobot bidang	jumlah skor BM25 tiap bidang × bobot: kepala 2,0 · pertimbangan 1,0 · amar 2,0 · penutup 0,5

Selain pencarian peringkat, tersedia model Boolean (AND, OR, NOT) dan pencarian frasa dalam tanda kutip.

4.4 Evaluasi

Tidak ada penilaian relevansi manual, sehingga dipakai silver standard: untuk 12 kueri bahasa alami, putusan relevan ditentukan otomatis dari atribut hasil ekstraksi (misalnya pekerjaan terdakwa, lama pidana, besar denda, isi amar, barang bukti). Metrik: MAP, nDCG@10, R-Precision, dan MRR pada 4 tahap praproses × 4 skema pembobotan (OUTPUT SUBCPMK 4/hasil_evaluasi.csv).

Praproses	Pembobotan	MAP	nDCG@10	R-Prec	MRR
D. + Stemming	BM25 berbobot bidang	0,864	0,894	0,809	0,878
C. + Normalisasi	BM25 berbobot bidang	0,845	0,884	0,778	0,878
A. Dasar	BM25 berbobot bidang	0,838	0,879	0,778	0,873
B. + Stopword	BM25 berbobot bidang	0,838	0,879	0,778	0,873
A. Dasar	BM25	0,740	0,754	0,719	0,800
A. Dasar	TF-IDF + cosine	0,727	0,755	0,712	0,838
D. + Stemming	BM25	0,734	0,750	0,694	0,801
D. + Stemming	TF-IDF + cosine	0,711	0,722	0,684	0,838
A. Dasar	TF mentah	0,268	0,300	0,203	0,436

(Tabel lengkap 16 kombinasi ada di hasil_evaluasi.csv; grafik pada perbandingan_metode.png.)

Temuan:

Konfigurasi terbaik adalah stemming + BM25 berbobot bidang (MAP 0,864), jauh di atas pembanding dasar TF mentah tanpa praproses (MAP 0,268).
Pembobotan memberi dampak terbesar. TF mentah memberi peringkat tertinggi pada dokumen terpanjang, sedangkan IDF dan normalisasi panjang pada TF-IDF dan BM25 menaikkan MAP dari ±0,27 menjadi ±0,73.
Bobot bidang menaikkan MAP BM25 dari ±0,74 menjadi ±0,84–0,86, karena atribut yang dicari (identitas terdakwa, amar) berada pada bidang kepala dan amar yang berbobot lebih tinggi.
Stemming membantu hanya pada BM25 berbobot bidang. Pada BM25 dan TF-IDF tanpa bobot bidang, tahap praproses tambahan tidak menambah MAP (selisih kecil).
Statistik indeks final: 50 dokumen, 3.618 term, ±343.000 token, 30.324 posting, rata-rata panjang dokumen ±6.860 token. Term seperti dakwa, narkotika, dan sabu muncul di 50 dari 50 putusan sehingga IDF-nya hampir nol (daya beda rendah). Distribusi frekuensi term mengikuti hukum Zipf (zipf.png).
4.5 Mesin pencari
cari(query, k): pencarian peringkat dengan metode terbaik, menampilkan nomor putusan, terdakwa, pidana penjara, dan cuplikan teks dengan kata kueri ditandai « ».
cari_boolean(query): operator AND, OR, NOT (huruf kapital) dan frasa "...". Contoh hasil: "permufakatan jahat" → 5 putusan; perempuan AND "rumah tangga" → 6; "sepeda motor" NOT perempuan → 12; "permufakatan jahat" OR pelajar → 15.
4.6 Berkas keluaran (OUTPUT SUBCPMK 4/)
Berkas	Isi
indeks_putusan.pkl	Inverted index (term, matriks TF, df, panjang dokumen, nomor putusan)
kamus_term.csv	3.618 term beserta df, cf, dan idf
korpus_praproses.csv	Token hasil praproses tiap putusan
ringkasan_putusan.csv	Metadata hasil ekstraksi tiap putusan
hasil_evaluasi.csv	16 kombinasi praproses × pembobotan
perbandingan_metode.png, zipf.png	Grafik evaluasi dan distribusi Zipf
txt/	50 teks penuh hasil ekstraksi
hasil_subcpmk4.zip	Paket seluruh keluaran
Cara Menjalankan

SUBCPMK-4 (Google Colab):

Buka colab.research.google.com → Upload → pilih UTS_IR_SUBCPMK4_Indexing.ipynb.
Jalankan Runtime → Run all. Notebook memasang pdfplumber dan PySastrawi, mengunduh Dataset/Narkotika.zip dari repository ini, lalu menjalankan seluruh tahap (±2 menit).
Hasil tersimpan di /content/hasil_subcpmk4 dan diunduh sebagai ZIP. Untuk menyimpan ke Google Drive, ubah SIMPAN_KE_DRIVE = True pada sel konfigurasi.

SUBCPMK-3 (VS Code): ikuti PANDUAN_VSCODE.md.

Mengambil dataset saja:

bash
git clone https://github.com/FakhriZiddanAkbar/Dataset-Narkotika_124_143.git
unzip Dataset/Narkotika.zip -d Dataset/
Keterbatasan Keseluruhan
Crawler: Direktori MA menolak akses otomatis (HTTP 403), sehingga metadata situs tidak berhasil dikumpulkan; data yang dipakai adalah hasil ekstraksi dari 50 PDF (lihat bagian 3.3).
Ekstraksi otomatis: barang bukti, amar, dan atribut terdakwa dibentuk dengan pola teks. Format penulisan yang tidak lazim dapat menggeser batas kutipan atau menghasilkan nilai janggal pada putusan tertentu (misalnya lama pidana kosong pada putusan 11/Pid.Sus/2024/PN Kkn). Gunakan PDF asli bila ketepatan kutipan penting.
Evaluasi: relevansi ditentukan otomatis dari atribut hasil ekstraksi (silver standard), bukan penilaian manual. Korpus hanya 50 putusan dan konfigurasi terbaik dipilih pada kueri yang sama dengan evaluasi, sehingga angka MAP bersifat indikatif, bukan estimasi performa umum.
Dua arsip PDF: Dataset/Narkotika.zip (dipakai SUBCPMK-2 dan SUBCPMK-4) dan Dataset/Putusan Pengadilan Negeri Kuala Kurun/Narkotika_Baru.zip (dipakai SUBCPMK-3) sama-sama berisi 50 PDF, tetapi berkas ZIP-nya tidak identik byte demi byte.
Keterlacakan sumber: URL per putusan dan tanggal akuisisi tidak tersedia sebagai kolom metadata. Status berkekuatan hukum tetap (BHT) tidak dapat disimpulkan dari metadata.
Cakupan korpus: terbatas pada 50 perkara sesuai tugas; kelengkapan terhadap seluruh putusan PN Kuala Kurun 2023–2025 tidak diverifikasi.
Referensi Sumber Resmi
Direktori Putusan Mahkamah Agung Republik Indonesia: sumber dokumen putusan.
Direktori Putusan: Narkotika dan Psikotropika: rujukan klasifikasi.
Situs Resmi Pengadilan Negeri Kuala Kurun: rujukan institusi pengadilan.

Untuk penggunaan akademis, cantumkan sumber resmi dan nomor putusan yang dirujuk. Untuk kepastian informasi perkara atau status BHT, lakukan verifikasi pada layanan resmi yang relevan.