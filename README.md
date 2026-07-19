# Restaurant Project (Zomato Data)

Notebook ini berisi proses **Data Understanding, Data Cleaning, Data Spesific Cleaning, dan Data Manipulation/Feature Engineering** untuk dataset Zomato.

pipeline analisis dan wrangling dari dataset hingga menghasilkan dataset yang lebih bersih untuk kebutuhan insight.

## Ringkasan Tahapan (dari notebook)
1. **Data Understanding**
   - Membaca data CSV
   - Mengecek dimensi data, tipe data, missing value, duplikasi, dan statistik deskriptif

2. **Data Cleaning (general cleaning)**
   - Menyeragamkan huruf menjadi lowercase
   - Menghapus spasi di awal/akhir
   - Menyeragamkan beberapa kolom teks (mis. `name`, `address`, `location`, dll.)

3. **Data Specific Cleaning**
   - Memperbaiki kolom `rate` (mengambil angka sebelum `/` lalu konversi ke numerik)
   - Memperbaiki `approx_cost(for two people)` menjadi numerik
   - Membersihkan kolom `phone` agar hanya berisi angka (simbol dibuang dan dikonversi ke format yang konsisten)
   - Menghapus duplikasi berdasarkan `name`, `address`, `location`
   - Menghapus baris yang `location` dan `cuisines`-nya kosong
   - Mengisi missing value:
     - `rate` memakai **median**
     - `approx_cost(for two people)` memakai **median**
     - `rest_type` memakai **modus**
     - `dish_liked` memakai **modus**

4. **Data Manipulation & Feature Engineering**
   - Membuat `total_reviews` dari `reviews_list` (mengubah list review jadi jumlah)
   - Membuat `has_menu` dari `menu_item` (menjadi 0/1)
   - Menghapus kolom asli `reviews_list` dan `menu_item` setelah fitur baru dibuat

5. **Business Use Case / Insight Visualisasi**
   - Bar chart: Top lokasi dengan jumlah restoran terbanyak
   - Pie chart: proporsi `online_order` (online vs offline)
   - Bar chart: 10 lokasi dengan rata-rata biaya makan termahal
   - Countplot: 10 tipe restoran terbanyak
   - Histogram: distribusi rating seluruh restoran

## Output
Notebook menghasilkan dataset yang sudah lebih bersih serta beberapa visualisasi insight bisnis.

