<template>
  <div class="container-fluid bg-white text-dark py-5">
    <h1 class="text-center mb-4 pb-4">Galeri</h1>
    <div class="row g-4">
      <div class="col-md-4" v-for="(image, index) in images" :key="index">
        <div class="card h-100 image-card">
          <img :src="image.src" :alt="image.title" class="card-img-top" />
          <div class="card-body">
            <h5 class="card-title">{{ image.title }}</h5>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import foto1 from "@/assets/img/foto1.png"
import foto2 from "@/assets/img/foto2.png"
import foto3 from "@/assets/img/foto3.png"
import foto4 from "@/assets/img/foto4.png"
import foto5 from "@/assets/img/foto5.png"
import foto6 from "@/assets/img/foto6.png"

const images = ref([
  { src: foto1, title: "Gambar 1" },
  { src: foto2, title: "Gambar 2" },
  { src: foto3, title: "Gambar 3" },
  { src: foto4, title: "Gambar 4" },
  { src: foto5, title: "Gambar 5" },
  { src: foto6, title: "Gambar 6" },
])

</script>

<style scoped>
.card-img-top {
  object-fit: cover;
  height: 200px;
  transition: transform 0.3s ease, filter 0.3s ease;
}

.image-card:hover .card-img-top {
  transform: scale(1.1);
  filter: brightness(0.8);
}

.card-body {
  text-align: center;
}
</style>