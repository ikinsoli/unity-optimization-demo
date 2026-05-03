# Real-Time Rendering Optimization Demo — Unity 6

Demo project implementasi dan analisis teknik optimasi real-time rendering menggunakan Unity 6.

## 📺 Video Demo
👉 https://youtu.be/9EALVn53P9A

## 📄 Laporan
Laporan ilmiah lengkap tersedia di repository ini:
`Laporan_RealTimeRendering_IkinSolihin_24130300007.pdf`

## 🛠 Tools
- Unity 6 (6000.0.41f1)
- Unity Statistics Panel

## ⚙️ Teknik Optimasi yang Diimplementasikan

### 1. Static Batching
Menggabungkan mesh objek statis ke dalam satu draw call untuk mengurangi CPU overhead.

| Metrik | Before | After |
|---|---|---|
| FPS | 136 | 90 |
| Batches | 113 | 6109 |
| Saved by Batching | 6083 | 0 |

### 2. Imposters (LOD)
Menggantikan mesh 3D kompleks dengan sprite 2D pada jarak jauh dari kamera.

| Metrik | Before | After |
|---|---|---|
| FPS | 287 | 264 |
| Frame Time | 3ms | 3.7ms |

### 3. Texture Optimization (Sprite Atlas)
Menggabungkan banyak tekstur ke dalam satu atlas untuk mengurangi draw calls.

| Metrik | Before | After |
|---|---|---|
| FPS | 267 | 248 |
| Batches | 8 | 5 |
| SetPass Calls | 8 | 5 |
| Saved by Batching | 0 | 4 |

## 📊 Kesimpulan
Optimasi rendering bukan soal menerapkan sebanyak mungkin teknik, tapi memahami kapan setiap teknik paling tepat digunakan.

## 🙏 Credit
Base project diadaptasi dari:
- [unity-optimization](https://github.com/SamuelAsherRivello/unity-optimization) by Samuel Asher Rivello (MIT License)
