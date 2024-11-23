# Prediksi Produksi Padi Menggunakan Regresi Linear

# created by : Matthew Raymond Hartono

## Deskripsi Proyek
Analisis ini bertujuan untuk memprediksi produksi padi di Indonesia berdasarkan data historis dari tahun 1970 hingga 2022. Proses ini dilakukan menggunakan model regresi linear sederhana dengan langkah-langkah berikut.

---

## Langkah-Langkah Analisis
### 1. Persiapan Data
- Data produksi padi diolah untuk menambahkan fitur **lagged production**, yaitu nilai produksi tahun sebelumnya, sebagai variabel input untuk model.
- Kolom ini membantu model mengenali pola temporal dalam data.

### 2. Pemisahan Data
- Data dibagi menjadi **70% untuk pelatihan (training)** dan **30% untuk pengujian (testing)**.
- Pemisahan dilakukan secara berurutan tanpa pengacakan (*shuffle*) agar tren waktu tetap terjaga.

### 3. Pelatihan Model
- Model regresi linear dilatih menggunakan data pelatihan untuk memahami hubungan antara produksi tahun sebelumnya dan produksi tahun berjalan.

### 4. Evaluasi Model
- Model diuji menggunakan data pengujian untuk mengukur performa dengan metrik berikut:
  - **Mean Squared Error (MSE):** Rata-rata kuadrat kesalahan prediksi.
  - **Root Mean Squared Error (RMSE):** Akar kuadrat dari MSE, dalam satuan produksi padi.
  - **Mean Absolute Percentage Error (MAPE):** Rata-rata persentase kesalahan absolut.

### 5. Prediksi Masa Depan
- Model digunakan untuk memprediksi produksi padi untuk tahun **2023** dan **2024** berdasarkan pola data historis.

---

## Hasil
### Evaluasi Model
- **MSE:** 36,788,069,362,837.19  
- **RMSE:** 6,065,316.92  
- **MAPE:** 5.56%  

### Prediksi Produksi Padi
- **2023:** 54,928,021.58 ton  
- **2024:** 55,502,340.65 ton  

---

## Catatan
Pendekatan ini menggunakan asumsi hubungan linier antara produksi padi di tahun-tahun berturut-turut. Untuk meningkatkan akurasi, model yang lebih kompleks seperti Random Forest atau LSTM dapat digunakan.
