<template>
  <div class="carousel">
    <div v-for="(slide, index) in slides" :key="index" class="carousel-slide" :class="{ active: index === activeSlide }">
      <img :src="slide.imgSrc" :alt="slide.caption">
      <div class="carousel-caption">{{ slide.caption }}</div>
    </div>
    <button class="carousel-control prev" @click="prevSlide">‹</button>
    <button class="carousel-control next" @click="nextSlide">›</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeSlide: 0,
      slides: [
        { imgSrc: 'https://via.placeholder.com/1024x480?text=Slide+1', caption: 'Slide 1' },
        { imgSrc: 'https://via.placeholder.com/1024x480?text=Slide+2', caption: 'Slide 2' },
        { imgSrc: 'https://via.placeholder.com/1024x480?text=Slide+3', caption: 'Slide 3' }
      ]
    };
  },
  methods: {
    prevSlide() {
      this.activeSlide = (this.activeSlide + this.slides.length - 1) % this.slides.length;
    },
    nextSlide() {
      this.activeSlide = (this.activeSlide + 1) % this.slides.length;
    }
  }
}
</script>

<style scoped>
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
  height: 300px; /* Sesuaikan dengan tinggi slide yang diinginkan */
}

.carousel-slide img {
  width: 100%;
  height: 100%;
  object-fit: cover; /* Memastikan gambar tidak terdistorsi */
}

.carousel-slide.active {
  display: block;
}

.carousel-caption {
  position: absolute;
  bottom: 20px;
  left: 50%;
  transform: translateX(-50%);
  background-color: rgba(0, 0, 0, 0.5); /* Warna latar belakang caption */
  color: #fff; /* Warna teks caption */
  padding: 10px;
  border-radius: 5px;
}

.carousel-control {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background-color: rgba(0, 0, 0, 0.5); /* Warna latar belakang tombol */
  color: #fff; /* Warna ikon tombol */
  border: none;
  font-size: 2rem;
  cursor: pointer;
  padding: 10px;
}

.carousel-control.prev {
  left: 10px;
}

.carousel-control.next {
  right: 10px;
}

.carousel-control:hover {
  background-color: rgba(0, 0, 0, 0.7); /* Warna latar belakang tombol saat dihover */
}

</style>
