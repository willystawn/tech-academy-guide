# 👣 OutSystems Booking App Guide

## Step 1. Create a New App
- Buka **OutSystems Service Studio**
- Pilih **New Application → Reactive Web App**
- Beri nama: `HotelBookingApp`

## Step 2. Define Entities
1. Buat entity `Hotel`  
   Kolom:
   - Name: Text
   - Location: Text
   - PricePerNight: Decimal
   - IsAvailable: Boolean (Default: True)

2. Buat entity `Booking`
   - UserId: Identifier
   - HotelId: Identifier
   - CheckIn: Date
   - CheckOut: Date
   - Status: Text (Default: "Pending")

## Step 3. Build the UI
- Buat **HomeScreen** → gunakan *List widget* untuk tampilkan hotel.
- Tambahkan tombol “Book Now” yang navigasi ke **BookingForm**.
- Buat **MyBookings** untuk menampilkan daftar pesanan user.

## Step 4. Add Business Logic
- Tambahkan **Server Action** `CreateBooking`:
  - Input: HotelId, CheckIn, CheckOut
  - Output: Booking record
- Lakukan kalkulasi `TotalPrice = DaysBetween(CheckIn, CheckOut) * PricePerNight`

## Step 5. Testing
- Jalankan aplikasi di browser
- Coba buat beberapa booking
- Pastikan data muncul di *MyBookings*

---

💡 **Tips**
Gunakan *Aggregates* untuk load data dari entity dan pastikan relasi antar entity sudah dihubungkan.
