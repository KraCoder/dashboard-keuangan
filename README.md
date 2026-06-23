# 💰 Dashboard Keuangan Keluarga

**Family Finance Dashboard** adalah aplikasi web single-page responsif untuk mengelola keuangan keluarga dengan fitur tracking transaksi, anggaran, reminder tagihan, dan visualisasi data.

## ✨ Fitur Utama

### 📊 Dashboard
- **Ringkasan Finansial**: Total saldo, pemasukan, pengeluaran, dan selisih bulan ini
- **Grafik Pengeluaran**: Visualisasi pie chart pengeluaran per kategori
- **Tren 6 Bulan**: Line chart untuk melihat tren pemasukan vs pengeluaran
- **Peringatan Aktif**: Alert real-time untuk anggaran yang terlampaui dan reminder tagihan

### 💳 Manajemen Transaksi
- Input transaksi manual (pengeluaran & pemasukan)
- Riwayat transaksi dengan filter per bulan, jenis, dan kategori
- Edit dan hapus transaksi
- Verifikasi transaksi bot (AI generated)
- 8 kategori transaksi: Makan, Transport, Utilitas, Hiburan, Jajan, Sewa, Kesehatan, Lainnya
- **Export Excel**: Download transaksi ke format XLSX

### 💵 Manajemen Dompet
- Kelola multiple wallet/account (Kas Tunai, Bank, E-Wallet)
- Tracking saldo real-time
- Edit nama, jenis, dan koreksi saldo
- Total saldo keluarga
- Otomatis update saldo setiap transaksi

### 📋 Anggaran (Budget)
- Set batas pengeluaran per kategori
- **Dua mode rentang**:
  - Per Bulan: Anggaran bulanan standard
  - Custom: Rentang tanggal custom (cocok untuk siklus gajian)
- Progress bar visual (hijau/kuning/merah)
- Alert saat mencapai 80% dan 100% dari batas
- Realisasi vs target tracking

### 🔔 Bill Reminder
- Tambah reminder tagihan bulanan
- Deteksi otomatis: sistem mendeteksi jika tagihan sudah dibayar via transaksi
- Notifikasi jatuh tempo (hari ini / besok / N hari lagi / terlambat)
- Catat pembayaran langsung ke transaksi
- Riwayat pembayaran

### ⚙️ Pengaturan
- Konfigurasi Supabase URL & Anon Key
- Test koneksi database
- Status koneksi real-time
- Reset konfigurasi

### 🌙 Tema & UI
- **Dark Mode**: Toggle tema gelap/terang dengan preferensi sistem
- **Responsive Design**: Optimal di mobile, tablet, dan desktop
- **Bottom Navigation** (Mobile): 5 tab utama
- **Sidebar** (Desktop): Navigation menu kiri untuk akses cepat
- **Mobile-first CSS**: Performance optimal untuk semua ukuran layar

### 🔐 Autentikasi
- Login dengan email & password (Supabase Auth)
- Multi-user support: Data terpisah per user
- Sesi persistent (remember login setelah refresh)
- Auto-sync across tabs

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Frontend** | HTML5, CSS3, Vanilla JavaScript (ES6+) |
| **Backend** | Supabase (PostgreSQL + Auth) |
| **Charts** | Chart.js 4.x |
| **Export** | XLSX (SheetJS) |
| **Deployment** | Vercel |

### Library yang Digunakan
```html
<script src="https://unpkg.com/@supabase/supabase-js@2"></script>
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script src="https://unpkg.com/xlsx/dist/xlsx.full.min.js"></script>
```

---

## 📂 Struktur Project

```
dashboard-keuangan/
├── index.html          # Single page application (all-in-one)
├── vercel.json         # Vercel deployment config
└── README.md           # Dokumentasi
```

**File tunggal** (`index.html`) berisi:
- **HTML**: Struktur UI + layout responsive
- **CSS**: Styling dengan CSS variables (dark mode support)
- **JavaScript**: Logika aplikasi & Supabase integration

---
## 🔒 Security & Privacy

### Best Practices
1. ✅ **Supabase Anon Key**: Aman digunakan untuk frontend (read/write terbatas)
2. ✅ **Row Level Security**: Data user terisolasi per user_id
3. ✅ **HTTPS Only**: Deployment di Vercel otomatis HTTPS
4. ✅ **No Local Passwords**: Credentials hanya di browser local storage

---

## 🤝 Contributing

Untuk improvement atau bug fixes:
1. Fork repository
2. Create feature branch: `git checkout -b feature/nama-fitur`
3. Commit changes: `git commit -m "Add fitur baru"`
4. Push: `git push origin feature/nama-fitur`
5. Create Pull Request

---

## 📄 License

Open source project. Free to use dan modify.

---

## 👨‍👩‍👧‍👦 Dibuat untuk Keluarga

💰 **Dashboard Keuangan Keluarga** dirancang untuk memudahkan keluarga mengelola keuangan bersama dengan transparansi, efisiensi, dan kemudahan.

---

## 📞 Support

- **Dokumentasi Supabase**: https://supabase.com/docs
- **Dokumentasi Chart.js**: https://www.chartjs.org/docs/latest/
- **Dokumentasi Vercel**: https://vercel.com/docs

---

**Last Updated**: June 2026 | **Version**: 1.0.0
