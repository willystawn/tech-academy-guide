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
