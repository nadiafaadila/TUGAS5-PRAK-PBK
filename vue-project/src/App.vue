<template>
  <div id="app">
    <Navbar />
    <Carousel />
    <div class="card-container">
      <Card v-for="product in products" :key="product.id" :product="product" />
    </div>
    <Footer />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Carousel from './components/Carouse1.vue';
import Card from './components/Card.vue';
import Footer from './components/Footer.vue';

export default {
  components: {
    Navbar,
    Carousel,
    Card,
    Footer
  },
  data() {
    return {
      products: [
        { id: 1, name: 'Produk 1', image: 'product1.jpg', description: 'Deskripsi produk 1' },
        { id: 2, name: 'Produk 2', image: 'product2.jpg', description: 'Deskripsi produk 2' },
        { id: 3, name: 'Produk 3', image: 'product3.jpg', description: 'Deskripsi produk 3' }
      ]
    }
  }
}
</script>

<style scoped>
/* Gaya CSS yang ditambahkan di sini */
/* Reset CSS */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* Body Styling */
body {
  font-family: 'Roboto', sans-serif;
  background-color: #f5f5f5;
  color: #333;
}

/* Navbar Styling */
nav {
  background-color: pink;
  padding: 10px 20px;
}

nav ul {
  list-style: none;
  display: flex;
}

nav ul li {
  margin-right: 20px;
}

nav ul li a {
  text-decoration: none;
  color: #fff;
  font-weight: bold;
  transition: color 0.3s ease;
}

nav ul li a:hover {
  color: #FFC107;
}

/* Carousel Styling */
.carousel {
  position: relative;
  overflow: hidden;
  margin: 20px 0;
}

.carousel-slide {
  display: none;
  position: absolute;
  width: 100%;
  height: 400px;
}

.carousel-slide img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.carousel-slide.active {
  display: block;
}

.carousel-caption {
  position: absolute;
  bottom: 20px;
  left: 50%;
  transform: translateX(-50%);
  background-color: rgba(0, 0, 0, 0.5);
  color: #fff;
  padding: 10px;
  border-radius: 5px;
}

/* Card Styling */
.card-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  margin: 0 auto;
  max-width: 1200px;
}

.card {
  width: 300px;
  background-color: #fff;
  margin: 20px;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.card img {
  width: 100%;
  height: auto;
  border-radius: 8px;
}

.card h2 {
  margin-top: 10px;
  color: #333;
}

.card p {
  color: #666;
}

.card button {
  background-color: #1976D2;
  color: #fff;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
  margin-top: 10px;
  transition: background-color 0.3s ease;
}

.card button:hover {
  background-color: #1565C0;
}

/* Footer Styling */
footer {
  color: rgb(125, 125, 248);
  text-align: center;
  left: 50;
  right: 30;
  width: 50%
}
</style>

