# 🛒 MOKASIR – Mobile Kasir & Sistem Inventori Retail

Aplikasi Point of Sale (POS) dan sistem inventori retail berbasis mobile yang dirancang untuk operasi kasir ritel. Dilengkapi dengan pemindaian barcode, pencetakan struk via Bluetooth, dan penyimpanan data lokal yang andal.

![Flutter](https://img.shields.io/badge/Flutter-3.1%2B-blue)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 📱 Fitur Utama

### 1. Pemindaian Barcode
- Pemindaian barcode produk menggunakan kamera hp secara real-time
- Mendukung berbagai format barcode (QR, EAN, UPC, dll)
- Animasi visual yang menarik saat pemindaian
- Indikator status kamera (aktif/nonaktif)

### 2. Sistem Keranjang & Kasir
- Tambah produk ke keranjang dengan cepat
- Pengaturan jumlah item (tambah/kurang)
- Perhitungan total otomatis
- Tampilan keranjang yang intuitif dan modern

### 3. Pembayaran & Struk
- Tampilan QR Code untuk pembayaran UPI
- Pencetakan struk langsung ke printer thermal Bluetooth
- Kustomisasi informasi toko pada struk
- Format tanggal dan jam sesuai locale Indonesia

### 4. Manajemen Produk
- Tambah produk baru dengan barcode dan harga
- Edit informasi produk yang sudah ada
- Hapus produk dari database
- Pencarian produk berdasarkan nama atau barcode

### 5. Pengaturan Toko
- Kustomisasi nama toko
- Alamat lengkap (2 baris)
- Nomor telepon
- ID UPI untuk pembayaran
- Teks footer struk (kustomisasi)

### 6. Dukungan Printer Bluetooth
- Integrasi dengan printer thermal Bluetooth
-_STATUS koneksi printer
- Pencetakan struk otomatis

### 7. Offline-First
- Penyimpanan data lokal menggunakan Hive
- Tidak memerlukan koneksi internet
- Data tersimpan dengan aman di perangkat

---

## 🏗 Arsitektur & Teknologi

Aplikasi ini dibangun menggunakan prinsip **Clean Architecture** dan **Feature-Driven Design** untuk memastikan skalabilitas dan maintainability kode.

| Kategori | Teknologi |
|----------|-----------|
| Framework | [Flutter](https://flutter.dev/) (SDK >=3.1.0) |
| State Management | flutter_bloc |
| Dependency Injection | get_it |
| Routing | go_router |
| Database Lokal | hive & hive_flutter |
| Pemindaian Barcode | mobile_scanner |
| Pencetakan Bluetooth | print_bluetooth_thermal |
| Data Modeling | json_serializable, equatable |
| Functional Programming | fpdart |
| Validasi | app_validators |

---

## 📋 Persyaratan Sistem

- Flutter SDK versi 3.1.0 atau lebih tinggi
- Android Studio / Xcode untuk emulator
- (Opsional) Perangkat Android/iOS fisik dan Printer Thermal Bluetooth untuk menguji fitur hardware

---

## 🚀 Cara Instalasi

### Langkah 1: Clone Repository
```bash
git clone <repository_url>
cd billing_app
```

### Langkah 2: Install Dependencies
```bash
flutter pub get
```

### Langkah 3: Generate Kode (Required untuk Hive)
```bash
dart run build_runner build --delete-conflicting-outputs
```

### Langkah 4: Jalankan Aplikasi
```bash
flutter run
```

---

## 📂 Struktur Proyek

```
lib/
├── config/                  # Konfigurasi aplikasi
│   └── routes/              # Definisi routing
├── core/                    # Komponen inti
│   ├── data/               # Konfigurasi database Hive
│   ├── error/              # Handling error
│   ├── service_locator/    # Dependency injection
│   ├── theme/              # Tema dan styling
│   ├── utils/              # Utility (validator, printer helper)
│   └── widgets/            # Widget yang bisa digunakan ulang
├── features/               # Fitur-fitur aplikasi
│   ├── billing/            # Fitur kasir & pembayaran
│   ├── product/           # Fitur manajemen produk
│   ├── settings/          # Fitur pengaturan
│   └── shop/              # Fitur detail toko
└── main.dart               # Entry point aplikasi
```

---

## 🖼 Tampilan Aplikasi

### Halaman Utama (Kasir)
- Tampilan scanner barcode di bagian atas
- Daftar item yang dipindai di bagian bawah
- Total harga yang dihitung otomatis
- Tombol menuju halaman kasir

### Halaman Kasir (Checkout)
- Ringkasan item yang dibeli
- Tampilan QR Code untuk pembayaran UPI
- Tombol cetak struk

### Manajemen Produk
- Daftar semua produk
- Tambah produk baru
- Edit produk
- Hapus produk

### Pengaturan
- Profil toko
- Menu manajemen produk
- Menu detail toko
- Pengaturan printer Bluetooth

---

## 🌐 Bahasa & Lokalisasi

- Semua teks antarmuka dalam bahasa Indonesia
- Format mata uang: Rupiah (Rp)
- Format tanggal: dd-MM-yyyy
- Format waktu: 24 jam

---

## 📄 Lisensi

Proyek ini dilisensikan di bawah MIT License.

---

## 👨‍💻 Pengembang

Aplikasi ini dibuat dengan ❤️ menggunakan Flutter.
