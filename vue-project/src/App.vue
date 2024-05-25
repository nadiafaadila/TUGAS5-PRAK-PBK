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
