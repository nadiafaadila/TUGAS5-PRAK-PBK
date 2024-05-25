<template>
  <div class="card">
    <img :src="product.image" :alt="product.name" />
    <h2>{{ product.name }}</h2>
    <p>{{ product.description }}</p>
    <div class="button-container">
      <button @click="deleteProduct">Beli Sekarang</button>
      <button @click="deleteProduct">Masukkan ke Keranjang</button>
      <button @click="deleteProduct" class="delete-btn">Hapus</button>
    </div>
  </div>
</template>


<script>
export default {
  name: 'Card',
  props: {
    product: Object
  },
  methods: {
    deleteProduct() {
      this.$emit('delete-product', this.product);
    }
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

.button-container {
  display: flex; /* Menggunakan flexbox */
  justify-content: space-between; /* Mengatur jarak yang sama antara tombol */
}

.card button {
  background-color: palevioletred; /* Warna latar belakang tombol */
  color: #fff; /* Warna teks tombol */
  border: none; /* Tanpa garis tepi */
  padding: 5px 10px; /* Padding tombol */
  border-radius: 5px; /* Sudut bulat tombol */
  cursor: pointer; /* Kursor berubah menjadi tangan saat dihover */
  transition: background-color 0.5s ease; /* Efek transisi saat dihover */
}

.card button:hover {
  background-color: pink; /* Warna latar belakang tombol saat dihover */
}

.card button.delete-btn {
  background-color: red; /* Warna latar belakang tombol delete */
  color: #fff; /* Warna teks tombol */
}

.card button.delete-btn:hover {
  background-color: rgb(236, 59, 59); /* Warna latar belakang tombol delete saat dihover */
}

</style>
