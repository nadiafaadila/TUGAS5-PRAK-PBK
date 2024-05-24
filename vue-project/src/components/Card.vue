<template>
  <div class="card">
    <img :src="product.image" :alt="product.name" />
    <h2>{{ product.name }}</h2>
    <p>{{ product.description }}</p>
    <button>Beli</button>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    product: Object
  }
}
</script>

<style scoped>
/* Card Styling */
.card {
  width: 300px; /* Lebar kartu */
  background-color: #fff; /* Warna latar belakang kartu */
  margin: 20px; /* Jarak antar kartu */
  padding: 20px; /* Padding di dalam kartu */
  border-radius: 8px; /* Sudut bulat */
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1); /* Bayangan kartu */
  transition: transform 0.3s ease; /* Efek transisi */
}

.card img {
  width: 100%; /* Ukuran gambar */
  height: auto; /* Menjaga aspek gambar */
  border-radius: 8px; /* Sudut bulat pada gambar */
}

.card h2 {
  margin-top: 10px; /* Jarak antara judul dan konten */
  color: #333; /* Warna teks judul */
}

.card p {
  color: #666; /* Warna teks konten */
}

.card button {
  background-color: #1976D2; /* Warna latar belakang tombol */
  color: #fff; /* Warna teks tombol */
  border: none; /* Tanpa garis tepi */
  padding: 10px 20px; /* Padding tombol */
  border-radius: 5px; /* Sudut bulat tombol */
  cursor: pointer; /* Kursor berubah menjadi tangan saat dihover */
  margin-top: 10px; /* Jarak antara konten dan tombol */
  transition: background-color 0.5s ease; /* Efek transisi saat dihover */
}

.card button:hover {
  background-color: #1565C0; /* Warna latar belakang tombol saat dihover */
}

</style>
