<template>
  <footer>
    <p>Hak Cipta &copy; 2024 Toko Online.</p>
  </footer>
</template>

<script>
export default {
  name: 'Footer'
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
</style>

  