# 🍞 Botani Bakery Queue Simulation

Repository ini merupakan implementasi penelitian simulasi antrian yang dirancang untuk menganalisis sistem pelayanan Botani Bakery. Penelitian berfokus pada pemodelan dinamika antrian dan evaluasi kinerja sistem melalui pendekatan **Discrete-Event Simulation (DES)**.

---

## 📚 Latar Belakang
Botani Bakery, salah satu kafe inovatif di lingkungan IPB Dramaga, menghadapi tantangan operasional berupa antrian panjang dan waktu tunggu tinggi terutama pada jam sibuk.  

⚠️ Dampak dari fenomena ini:
- Menurunnya kepuasan pelanggan  
- Potensi kehilangan pelanggan (*potential loss of customers*)  
- Inefisiensi operasional  

📌 Observasi awal menunjukkan bahwa sistem pelayanan saat ini belum optimal dalam menghadapi fluktuasi kedatangan pelanggan.

---

## 🎯 Tujuan
Penelitian ini bertujuan untuk:
1. Memodelkan sistem antrian existing di Botani Bakery berdasarkan data observasi.  
2. Menganalisis kinerja sistem antrian current melalui simulasi komputer.  
3. Mengevaluasi berbagai skenario improvement untuk mengurangi waktu tunggu dan panjang antrian.  
4. Memberikan rekomendasi berbasis data untuk perbaikan sistem pelayanan.  

---

## 🧩 Model Simulasi
Model dikembangkan berdasarkan **data observasi lapangan** dengan proses **parameter fitting** untuk menentukan distribusi probabilitas yang sesuai.  

Karakteristik sistem yang dimodelkan:
- Pola kedatangan pelanggan yang stochastic  
- Mekanisme pelayanan dua tahap: loket pemesanan & loket pembayaran  
- Variasi ukuran grup pelanggan  
- Preferensi layanan (dine-in vs take-away)  
- Kapasitas terbatas pada antrian dan area dine-in  
- Kemungkinan pesanan ulang (reordering behavior)  

---

## 📂 Struktur Repository
```
Botani-Bakery-Queue-Simulation/
├── Antrian Normal.ipynb                 # Implementasi model dasar
├── Penambahan Server SnackBox.ipynb     # Skenario eksperimen
├── Parameter Fitting.ipynb              # Analisis fitting parameter
├── Data Pengamatan Pelanggan.xlsx       # Data observasi lapangan
├── Hasil Running.xlsx                   # Output hasil simulasi
├── Flowchart.png                        # Diagram alir proses
└── README.md                            # Dokumentasi penelitian
```
---

## 🛠️ Teknologi dan Tools
- **Bahasa Pemrograman**: `Julia (v1.x)`  
- **Framework Simulasi**: `ConcurrentSim.jl`  
- **Analisis Statistik**: `Distributions.jl`, `HypothesisTests.jl`  
- **Visualisasi**: `Plots.jl`, `StatsPlots.jl`  
- **Environment**: `Jupyter Notebook`  
- **Version Control**: `Git/GitHub`  

---

## 🧪 Penelitian dan Eksperimen

Pendekatan: **Discrete-Event Simulation (DES)**  
Dilakukan melalui dua skenario eksperimen utama:

### 1. 📊 Eksperimen Antrian Normal (Existing System)  
- Dua server pada loket pemesanan & loket pembayaran  
- Merepresentasikan kondisi current tanpa modifikasi  

📌 **Hasil**:
- Rata-rata panjang antrian: 7 pelanggan di kedua loket  
- Waktu tunggu rata-rata: 9 menit (loket pemesanan), 3 menit (loket pembayaran)  
- 23 pelanggan meninggalkan antrian (balk)
- jumlah pelanggan yang datang sebanyak 198 orang  

---

### 2. 🚀 Eksperimen Penambahan Server Snackbox (Improvement Scenario)  
- Menambahkan server khusus untuk menangani pesanan snackbox  
- Mengatasi bottleneck pada pesanan besar dengan waktu pengemasan lebih lama  

📌 **Hasil**:
- Rata-rata panjang antrian loket turun menjadi hanya 1 pelanggan
- Waktu tunggu rata-rata: 27 detik (loket pemesanan), 40 detik (loket pembayaran)  
- Tidak ada pelanggan yang meninggalkan antrian (balk)
- Jumlah pelanggan meningkat menjadi 205 orang
  
---

## ✅ Kesimpulan
Hasil simulasi menunjukkan bahwa penambahan server khusus untuk snackbox merupakan intervensi yang efektif untuk mengurangi panjang antrian, mempercepat waktu tunggu, dan meningkatkan efisiensi sistem pelayanan. Dengan demikian, strategi ini direkomendasikan sebagai **solusi berbasis bukti (evidence-based improvement)** bagi Botani Bakery.  
