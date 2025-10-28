# Tugas 1: Membuat Komponen Daftar Kamar (Room List)

## 🎯 Objektif

Buat sebuah komponen React yang menampilkan daftar kamar hotel dari data yang telah disediakan. Komponen ini harus menampilkan informasi utama setiap kamar dan menyediakan fungsionalitas dasar seperti tombol edit.

## ✅ Kriteria Penerimaan (Acceptance Criteria)

1.  **Tampilan Daftar:** Komponen berhasil menampilkan daftar kamar dalam bentuk tabel atau kartu (pilih salah satu).
2.  **Kolom Data:** Setiap item kamar harus menampilkan informasi berikut:
    *   Nama Kamar (contoh: "Deluxe Room")
    *   Tipe Kamar (contoh: "Double Bed")
    *   Harga per Malam (contoh: "Rp 1.500.000")
3.  **Tombol Aksi:** Setiap item kamar harus memiliki tombol "Edit". Untuk saat ini, tombol ini belum perlu memiliki fungsi, cukup tampilkan saja.
4.  **Data Statis:** Gunakan data sampel yang disediakan di bawah ini langsung di dalam kode Anda (hardcoded).

##  constraining Kendala (Constraints)

*   Gunakan fungsional komponen React dan hooks.
*   Styling harus menggunakan Tailwind CSS.

## 📊 Data Sampel (Sample Data)

Gunakan array JavaScript berikut sebagai sumber data Anda:

```javascript
const rooms = [
  { id: 1, name: 'Deluxe Room', type: 'Double Bed', price: 1500000 },
  { id: 2, name: 'Standard Room', type: 'Single Bed', price: 850000 },
  { id: 3, name: 'Suite Room', type: 'King Bed', price: 2500000 }
];
```

## ✨ Hasil yang Diharapkan

Sebuah halaman web yang menampilkan tiga kamar dari data sampel, masing-masing dengan nama, tipe, harga, dan sebuah tombol "Edit".

# 🏨 OutSystems Challenge: Booking Hotel App

## 🎯 Objective
Buat aplikasi pemesanan hotel sederhana di OutSystems yang memungkinkan pengguna:
- Melihat daftar hotel yang tersedia
- Melakukan pemesanan kamar
- Melihat riwayat booking mereka

## 🧱 Requirements

### 1. Entity & Data Model
Buat tiga entitas:
- **Hotel** (Id, Name, Location, PricePerNight)
- **Booking** (Id, UserId, HotelId, CheckIn, CheckOut, Status)
- **User** (Id, Name, Email)

Lihat contoh model di `/challenge/assets/data-model.png`.

### 2. Screens
- **HomeScreen**: Menampilkan daftar hotel
- **BookingForm**: Form untuk melakukan booking
- **MyBookings**: Daftar riwayat pemesanan pengguna

### 3. Logic
- Hanya tampilkan hotel yang `IsAvailable = True`
- Hitung total harga berdasarkan `CheckOut - CheckIn`
- Simpan booking baru ke entity `Booking`

### 4. Style & UI
Gunakan tema default OutSystems Reactive App.
Tambahkan elemen desain yang bersih (lihat `/challenge/assets/sample-ui.png`).

### 5. Bonus Challenge 🌟
- Tambahkan fitur filter hotel berdasarkan lokasi.
- Tambahkan notifikasi popup setelah user sukses booking.

## 🧪 Evaluation Criteria
| Kriteria | Deskripsi | Bobot |
|-----------|------------|-------|
| Functionality | Fitur berjalan sesuai deskripsi | 40% |
| Logic | Validasi dan kalkulasi benar | 25% |
| UI/UX | Tampilan rapi dan konsisten | 20% |
| Code Quality | Naming, modularitas, dan maintainability | 15% |

---

📦 **Deliverables**
- File `.oml` dari OutSystems
- Screenshot dari setiap screen
- Link deploy (jika dipublikasikan ke OutSystems Cloud)
