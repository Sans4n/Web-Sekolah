<script setup>
import { ref } from 'vue';

// Data fasilitas
const facilities = ref([
    {
        id: 1,
        title: 'Laboratorium RPL',
        image: '/assets/ruangan/RPL.jpg',
    },
    {
        id: 2,
        title: 'Laboratorium TBSM',
        image: '/assets/ruangan/TBSM.jpg',
    },
    {
        id: 3,
        title: 'Masjid',
        image: '/assets/ruangan/masjid.jpg',
    },
    {
        id: 4,
        title: 'Laboratorium TKJ',
        image: '/assets/ruangan/TJKT.jpg',
    },
    {
        id: 5,
        title: 'Parkiran Motor',
        image: '/assets/ruangan/foto10.jpg',
    },
    {
        id: 6,
        title: 'Laboratorium DKV',
        image: '/assets/ruangan/DKV.jpg',
    },
]);
</script>

<template>
    <div class="container mt-4">
        <h1 class="text-center mb-4">Fasilitas Sekolah</h1>

        <!-- Daftar Fasilitas -->
        <div class="row">
            <div v-for="facility in facilities" :key="facility.id" class="col-lg-4 col-md-6 col-sm-12 mb-4">
                <div class="card shadow-sm">
                    <img :src="facility.image" alt="Facility Image" class="card-img-top" />
                    <div class="card-body text-center">
                        <h5 class="card-title">{{ facility.title }}</h5>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.card {
    border-radius: 10px;
}

.card-img-top {
    height: 200px;
    object-fit: cover;
}
</style>