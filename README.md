# T1_WEB_SCRAPING

Latar Belakang Pemilihan Tempo:

-Tempo dikenal sebagai media berita yang kredibel dan independen sejak lama, sehingga data yang diambil lebih dapat dipercaya.

-Menyajikan topik yang beragam mulai dari politik, ekonomi, teknologi, hingga gaya hidup sehingga datanya lebih kaya.

-Struktur website cukup rapi sehingga memudahkan proses scraping menggunakan BeautifulSoup.

-Publikasi berita yang konsisten membuat dataset selalu up-to-date untuk kebutuhan analisis.

Latar Belakang Pemilihan CNN Indonesia:

-CNN Indonesia merupakan portal berita terpercaya dengan reputasi internasional yang tinggi.

-Menyediakan cakupan berita yang luas, mulai dari isu nasional hingga global, sehingga relevan untuk berbagai analisis.

-Memiliki struktur halaman yang jelas dan stabil sehingga mendukung proses scraping lebih mudah.

-Kontennya selalu diperbarui secara rutin, menjadikan hasil scraping lebih relevan dan aktual.

Kesimpulan:
Pemilihan portal berita Tempo dan CNN Indonesia didasarkan pada kredibilitas dan reputasi keduanya sebagai sumber informasi terpercaya di Indonesia. Keduanya menyajikan konten yang beragam dan selalu diperbarui, dengan struktur website yang rapi sehingga memudahkan proses scraping. Hal ini menjadikan Tempo dan CNN Indonesia sebagai sumber data yang relevan, akurat, dan layak digunakan untuk analisis lebih lanjut.

Baik, berikut **alur scraping Tempo dalam bentuk teks saja** tanpa diagram visual:

---

Alur Scraping Tempo

1. **Import Library**

   * Program memanggil requests, BeautifulSoup, pandas, dan json sebagai alat untuk mengambil data, parsing XML, mengolah tabel, serta menyimpan hasil dalam berbagai format.

2. **Definisi Daftar RSS Feed Tempo**

   * Dibuat dictionary berisi kategori berita (Nasional, Bisnis, Metro, dll.) beserta URL RSS masing-masing.

3. **Looping Kategori**

   * Program membaca setiap kategori dalam dictionary.
   * Menggunakan requests untuk mengambil konten RSS feed.
   * Parsing hasil dengan BeautifulSoup menggunakan parser "xml".

4. **Ekstraksi Data Artikel**

   * Dari tiap RSS feed, program mencari semua elemen `<item>`.
   * Untuk setiap `<item>`, diambil data berikut:

     * **category** (kategori berita, misalnya Nasional, Bisnis, dll.)
     * **title** (judul artikel)
     * **link** (tautan artikel)
     * **date** (tanggal publikasi)
     * **summary** (deskripsi singkat dari artikel)
   * Semua hasil disimpan dalam list `articles`.

5. **Konversi ke DataFrame**

   * List `articles` diubah menjadi tabel menggunakan `pandas.DataFrame` agar lebih mudah diproses dan diekspor.

6. **Ekspor Hasil**

   * Data diekspor ke tiga format:

     * **CSV** → `tempo_articles.csv`
     * **XLSX (Excel)** → `tempo_articles.xlsx`
     * **JSON** → `tempo_articles.json`

7. **Output Hasil**

   * Program menampilkan jumlah artikel yang berhasil dikumpulkan.
   * Menampilkan preview 20 artikel pertama untuk memastikan hasil sesuai.

---

Jadi alurnya: **ambil RSS feed → parsing XML → ekstrak artikel → simpan ke list → konversi ke DataFrame → ekspor ke CSV/XLSX/JSON → tampilkan ringkasan hasil.**

Mau saya buatkan juga versi **step-by-step eksekusi contoh nyata** (misalnya scraping 1 kategori RSS Nasional sampai jadi file CSV/JSON)?
