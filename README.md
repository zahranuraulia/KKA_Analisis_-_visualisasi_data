## 1. Analisis Produk Underperformer
**Business Question:** Kategori mana yang memiliki harga tinggi namun jarang laku?

**Temuan Analisis:**
Melalui metode *Quadrant Analysis*, kami menemukan bahwa kategori [Sebutkan Nama Kategori] berada di zona **Underperformer**. 
- **Masalah:** Harga per unit jauh di atas rata-rata (High Price), namun total kuantitas terjual sangat rendah (Low Volume).
- **Dampak:** Inefisiensi stok dan arus kas terhambat karena modal tertahan pada barang yang lambat terjual.
**Kesimpulan:** Harga yang tinggi pada kategori ini menjadi penghambat volume penjualan. Dibutuhkan penyesuaian harga atau strategi promosi agresif.

  ## 2. Data Wrangling & Cleaning
**Business Question:** Apakah data sudah valid dan siap untuk diolah?

**Proses yang Dilakukan:**
1. **Konversi Tipe Data:** Mengubah kolom `Order_Date` dari format teks menjadi *datetime* untuk memungkinkan perhitungan analisis waktu (Recency).
2. **Handle Missing Values:** Memeriksa nilai yang hilang pada kolom krusial seperti `CustomerID` dan `Total_Sales`. (Hasil: Data bersih, tidak ada nilai null).
3. **Standarisasi Kategori:** Melakukan pengecekan pada kolom `Product_Category` untuk memastikan tidak ada duplikasi nama kategori akibat perbedaan penulisan huruf kapital.
4. **Perhitungan Kolom Baru:** Membuat kolom `Efficiency_Ratio` (Total Sales / Ad Budget) untuk menjawab kebutuhan analisis efisiensi iklan.

**Kesimpulan:** Data telah melewati tahap validasi dan pembersihan, sehingga hasil analisis pada tahap selanjutnya memiliki tingkat akurasi yang tinggi.

## 3. Analisis Efisiensi Anggaran Iklan
**Business Question:** Kategori mana yang memberikan hasil penjualan terbaik dari setiap rupiah biaya iklan?
<img width="1255" height="785" alt="image" src="https://github.com/user-attachments/assets/2b8f1230-8a67-40c0-bfac-cb39c08e4b89" />

### 📈 Insights: Analisis Kontribusi & Efisiensi
Berdasarkan visualisasi Bar Chart Efisiensi, ditemukan pola sebagai berikut:

- **Efisien (Top Performer):** Kategori **Electronics** memimpin dengan rasio **1.44**. Strategi iklan di sini terbukti sangat sukses dan memberikan imbal balik keuntungan tertinggi bagi perusahaan.
- **Moderat:** Kategori **Books** dan **Fashion** menunjukkan performa yang konsisten di sekitar rata-rata efisiensi perusahaan.
- **Inefisien (Warning):** Kategori **Gadget** (0.92) adalah yang paling tidak efisien. Perusahaan menghabiskan banyak biaya namun hasil penjualannya paling rendah secara proporsional.

**Kesimpulan:** Tidak semua anggaran iklan memberikan dampak yang sama. Investasi pada kategori Electronics memberikan hasil yang jauh lebih pasti dibandingkan Gadget.

## 🚀 4. Recommendation
Berdasarkan temuan data, kami menyarankan langkah-langkah berikut:

1. **Efisiensi Iklan:** Alihkan budget iklan dari kategori **Gadget** ke **Electronics** untuk memaksimalkan keuntungan, mengingat rasio efisiensi Electronics jauh lebih unggul (1.44 vs 0.92).
2. **Likuidasi Stok:** Lakukan promo khusus untuk produk di kategori **Home Decor** guna mengurangi beban arus kas akibat barang yang lama tersimpan (Underperformer).
3. **Personalized Marketing:** Gunakan data segmen **Champions** hasil RFM Analysis untuk program *Loyalty Reward* tanpa harus membakar budget iklan pada segmen pelanggan yang tidak aktif (*Lost*).
4. **Audit Harga:** Evaluasi kembali struktur harga pada kategori yang memiliki efisiensi rendah untuk memastikan daya saing di pasar.


