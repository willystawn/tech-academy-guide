# Panduan Lengkap: Membuat Komponen Daftar Kamar

Berikut adalah langkah-langkah detail untuk menyelesaikan tugas ini dari awal hingga akhir.

### Langkah 1: Buat File Komponen

Pertama, buat file baru di dalam direktori `src/components/` dengan nama `RoomList.jsx`.

### Langkah 2: Struktur Dasar Komponen

Isi file `RoomList.jsx` dengan struktur dasar komponen React dan data sampel.

```jsx
import React from 'react';

// Data sampel yang akan kita tampilkan
const rooms = [
  { id: 1, name: 'Deluxe Room', type: 'Double Bed', price: 1500000 },
  { id: 2, name: 'Standard Room', type: 'Single Bed', price: 850000 },
  { id: 3, name: 'Suite Room', type: 'King Bed', price: 2500000 }
];

const RoomList = () => {
  return (
    <div className="p-8">
      <h1 className="text-2xl font-bold mb-4">Daftar Kamar Hotel</h1>
      {/* Kita akan me-render daftar kamar di sini */}
    </div>
  );
};

export default RoomList;
```
### Langkah 3: Render Daftar Kamar Menggunakan .map()

Sekarang, kita akan menggunakan metode .map() untuk mengubah setiap objek di dalam array rooms menjadi elemen JSX. Kita akan menampilkannya dalam bentuk kartu (card).

Tambahkan kode ini di dalam div utama pada RoomList.jsx.

```jsx
// ... (kode sebelumnya)

const RoomList = () => {
  // Fungsi untuk memformat harga menjadi Rupiah
  const formatPrice = (price) => {
    return new Intl.NumberFormat('id-ID', {
      style: 'currency',
      currency: 'IDR',
      minimumFractionDigits: 0
    }).format(price);
  };

  return (
    <div className="p-8 max-w-4xl mx-auto">
      <h1 className="text-2xl font-bold mb-6">Daftar Kamar Hotel</h1>
      <div className="space-y-4">
        {rooms.map((room) => (
          <div key={room.id} className="flex items-center justify-between p-4 border rounded-lg shadow-sm bg-white">
            <div>
              <h2 className="text-lg font-semibold">{room.name}</h2>
              <p className="text-gray-600">{room.type}</p>
              <p className="text-gray-800 font-medium mt-1">{formatPrice(room.price)} / malam</p>
            </div>
            <button className="px-4 py-2 bg-blue-500 text-white rounded-md hover:bg-blue-600">
              Edit
            </button>
          </div>
        ))}
      </div>
    </div>
  );
};

export default RoomList;
```

### Langkah 4: Tampilkan Komponen di Halaman Utama

Terakhir, pastikan komponen RoomList ditampilkan. Buka file src/App.jsx dan impor komponen RoomList, lalu render di dalamnya.

```jsx
import React from 'react';
import RoomList from './components/RoomList';

function App() {
  return (
    <div className="bg-gray-50 min-h-screen">
      <RoomList />
    </div>
  );
}

export default App;
```

Sekarang, jika Anda menjalankan aplikasi, Anda seharusnya melihat daftar kamar yang telah di-styling dengan Tailwind CSS.