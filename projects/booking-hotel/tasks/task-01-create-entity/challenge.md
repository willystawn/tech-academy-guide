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