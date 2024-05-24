<template>
  <nav>
    <ul>
      <li><a href="#">Beranda</a></li>
      <li><a href="#">Produk</a></li>
      <li><a href="#">Tentang Kami</a></li>
      <li><a href="#">Kontak</a></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Navbar'
}
</script>

<style>
/* Navbar Styling */
nav {
background-color: pink;
padding: 20px;
position: fixed; /* Navbar tetap di atas halaman */
top: 0; /* Membuat navbar menempel di bagian atas */
left: 0;
right: 0;
z-index: 1000; /* Menempatkan navbar di atas konten lain */
width: 100%; /* Lebar navbar */
}

nav ul {
list-style: none;
display: flex; /* Menjadikan menu horizontal */
}

nav ul li {
margin-right: 30px; /* Jarak antar item menu */
}

nav ul li a {
text-decoration: none; /* Menghilangkan dekorasi link */
color: #fff; /* Warna teks */
font-weight: bold; /* Tebalkan teks */
transition: color 0.3s ease; /* Efek transisi ketika hover */
}

nav ul li a:hover {
color: black;
}
</style>
