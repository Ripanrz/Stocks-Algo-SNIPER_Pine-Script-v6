# 🎯 Stocks Algo SNIPER (Pine Script v6)

![Pine Script Version](https://img.shields.io/badge/Pine%20Script-v6-blue?style=for-the-badge&logo=tradingview)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Stable-brightgreen?style=for-the-badge)

**Stocks Algo SNIPER** adalah indikator teknikal mutakhir untuk platform TradingView yang berfokus pada strategi *Trend-Following Pullback*. Script ini dirancang khusus untuk trader saham dan aset dengan volatilitas tinggi yang mengutamakan presisi entri dan manajemen risiko otomatis.

---

## 🚀 Fitur Unggulan

- **Advanced Trend Filtering:** Menggunakan EMA 200 sebagai "kompas" arah tren utama.
- **Precision Rejection Logic:** Sinyal hanya muncul jika terjadi konfirmasi *rejection* pada EMA 20, mengurangi risiko terjebak dalam koreksi tajam.
- **Dynamic Risk Management:** Menghitung Stop Loss (SL) dan Take Profit (TP) secara dinamis menggunakan *Average True Range* (ATR).
- **Self-Cleaning UI:** Sistem cerdas yang menghapus objek (garis & label) lama secara otomatis saat trade selesai atau sinyal baru muncul, menjaga chart Anda tetap bersih.
- **Scalable Architecture:** Kode ditulis secara modular sehingga mudah dimodifikasi untuk penambahan filter tambahan seperti Volume atau RSI.

---

## 🛠️ Cara Kerja Strategi

Indikator ini mengikuti aturan baku **"Mean Reversion within a Trend"**:

1. **Uptrend Check:** Harga > EMA 200.
2. **Pullback Zone:** Harga mendekati atau menyentuh EMA 20.
3. **Confirmation:** Candle harus menunjukkan penolakan (*Bullish Rejection* untuk Buy, *Bearish Rejection* untuk Sell).
4. **Execution:** Plotting otomatis harga Entry (Garis Biru), Stop Loss (Garis Merah), dan Take Profit (Garis Hijau).

---

## ⚙️ Parameter Input

| Parameter | Default | Deskripsi |
| :--- | :--- | :--- |
| **ATR Period** | 22 | Periode untuk perhitungan volatilitas dasar. |
| **ATR Multiplier** | 3.0 | Pengali untuk menentukan target profit (Risk/Reward). |
| **Max Labels/Lines** | 500 | Batas maksimal objek agar tidak membebani performa browser. |

---

## 📥 Instalasi

1. Buka **Pine Editor** di TradingView.
2. Buat file baru (**Open -> New Indicator**).
3. Hapus semua kode default, lalu tempelkan kode dari file `sniper_fixed.pinescript`.
4. Klik **Save** lalu **Add to Chart**.
5. Selesai! Indikator siap digunakan.

---

## 📦 Skalabilitas & Kustomisasi

Script ini dirancang untuk dikembangkan lebih lanjut. Anda bisa menambahkan filter berikut ke dalam blok `SIGNAL LOGIC`:
- **Volume Filter:** `and volume > ta.sma(volume, 20)`
- **RSI Filter:** `and ta.rsi(close, 14) < 70`

---

## 📜 Lisensi & Disclaimer

Proyek ini berada di bawah lisensi **MIT**. 

**Disclaimer:** Trading memiliki risiko kerugian finansial yang nyata. Indikator ini adalah alat bantu keputusan, bukan nasihat keuangan. Lakukan *backtest* secara menyeluruh sebelum menggunakan modal riil.

---
