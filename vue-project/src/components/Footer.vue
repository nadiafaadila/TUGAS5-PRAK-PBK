Tentu, berikut adalah contoh gaya untuk tombol "Hapus Semua Data":

```html
<template>
  <footer>
    <p>Hak Cipta &copy; 2024 Nanad BeautyCare.</p>
    <button @click="deleteAllData" class="delete-all-btn">Hapus Semua Data</button>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  methods: {
    deleteAllData() {
      // Emit event 'delete-all-data' ke komponen induk
      this.$emit('delete-all-data');
    }
  }
}
</script>

<style scoped>
/* Footer Styling */
footer {
  color: blue; /* Warna teks footer */
  text-align: center; /* Teks rata tengah */
  padding: 10px 0; /* Padding atas dan bawah */
  position: fixed; /* Footer akan tetap di bagian bawah layar */
  width: 50%; /* Lebar footer */
  bottom: 0; /* Footer akan melekat pada bagian bawah */
  left: 50%; /* Footer akan dimulai dari tengah */
  transform: translateX(-50%); /* Menyentuh bagian bawah dari tengah */
}

footer p {
  margin: 0; /* Menghapus margin default pada teks */
}

.delete-all-btn {
  background-color: #f44336; /* Warna latar belakang tombol */
  color: #fff; /* Warna teks tombol */
  border: none; /* Tanpa garis tepi */
  padding: 3px 10px; /* Padding tombol */
  border-radius: 5px; /* Sudut bulat tombol */
  cursor: pointer; /* Kursor berubah menjadi tangan saat dihover */
  transition: background-color 0.5s ease; /* Efek transisi saat dihover */
}

.delete-all-btn:hover {
  background-color: #d32f2f; /* Warna latar belakang tombol saat dihover */
}
</style>