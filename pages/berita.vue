<script setup>
import { ref, computed } from 'vue';

const newsList = ref([
    {
        id: 1,
        title: 'AHM Resmikan Safety Riding Lab di SMKN 4 Tasikmalaya, Wujudkan Komitmen Keselamatan Berkendara',
        image: 'https://assets.radartasik.id/main/2024/05/Duta-Safety-Riding-SMKN-4-Tasikmalaya-.webp',
        url: 'https://radartasik.id/2024/05/21/ahm-resmikan-safety-riding-lab-di-smkn-4-tasikmalaya-wujudkan-komitmen-keselamatan-berkendara/',
    },
    {
        id: 2,
        title: 'Sinergi Bagi Negeri, DAM Jalin Kerjasama Dengan SMKN 4 Tasikmalaya Terapkan Kurikulum Teknik & Bisnis Sepeda Motor',
        image: 'https://assets.promediateknologi.id/crop/0x0:0x0/750x500/webp/photo/2023/03/03/WhatsApp-Image-2023-03-03-at-195922-656889757.jpeg',
        url: 'https://www.radarcianjur.com/jabar/9457833134/sinergi-bagi-negeri-dam-jalin-kerjasama-dengan-smkn-4-tasikmalaya-terapkan-kurikulum-teknik-bisnis-sepeda-m',
    },
    {
        id: 3,
        title: 'SMKN 4 Tasikmalaya Koneksikan Iduka dengan Pencari Kerja',
        image: 'https://assets.radartasik.id/main/2023/10/SMKN-4-300x178.jpg',
        url: 'https://radartasik.id/2023/10/12/smkn-4-tasikmalaya-koneksikan-iduka-dengan-pencari-kerja/',
    },
    {
        id: 4,
        title: 'SMKN 4 Tasikmalaya Gelar Job Fair 2023, Harapkan Angka Pengangguran di Tasikmalaya Berkurang',
        image: 'https://ruangatas.com/wp-content/uploads/2023/10/Picsart_23-10-12_16-15-19-734-1536x864.jpg',
        url: 'https://ruangatas.com/smkn-4-tasikmalaya-gelar-job-fair-2023-harapkan-angka-pengangguran-di-tasikmalaya-berkurang/',
    },
    {
        id: 5,
        title: '320 Pesilat Perisai Diri Ikuti UKT Periode 72 di SMKN 4 Tasikmalaya, Penerimaan Anggota Baru Dibuka',
        image: 'https://assets.pikiran-rakyat.com/crop/12x0:1228x612/x/photo/2024/07/14/1530137579.png',
        url: 'https://kabarpriangan.pikiran-rakyat.com/kabar-priangan/pr-1488326544/320-pesilat-perisai-diri-ikuti-ukt-periode-72-di-smkn-4-tasikmalaya-penerimaan-anggota-baru-dibuka?page=all',
    },
]);

const displayedNews = ref([...newsList.value.slice(0, 3)]);

const limitStart = ref(displayedNews.value.length);
const limitEnd = ref(limitStart.value + 4);


const loadMoreNews = () => {
    displayedNews.value = [...displayedNews.value, ...newsList.value.slice(limitStart.value, limitEnd.value)];
    limitStart.value = limitEnd.value;
    limitEnd.value += 4;
};


const allNewsLoaded = computed(() => limitStart.value >= newsList.value.length);
</script>

<template>
    <div class="container mt-4">
        <h1 class="text-center mb-4">Halaman Berita</h1>
        <div class="row">
            <div class="col-md-4 mb-4" v-for="news in displayedNews" :key="news.id">
                <div class="card shadow-sm">
                    <img :src="news.image" alt="News Image" class="card-img-top" />
                    <div class="card-body">
                        <h5 class="card-title">{{ news.title }}</h5>
                        <p class="card-text">{{ news.description }}</p>
                    </div>
                    <div class="card-footer text-center">
                        <a :href="news.url" target="_blank" class="btn btn-primary">
                            Baca Selengkapnya
                        </a>
                    </div>
                </div>
            </div>
        </div>
        <div class="text-center mt-3 py-5">
            <button class="btn btn-primary" @click="loadMoreNews" :disabled="allNewsLoaded">
                {{ allNewsLoaded ? 'Semua Berita Dimuat' : 'Muat Lebih Banyak' }}
            </button>
        </div>
    </div>
</template>

<style>
.card {
    border-radius: 10px;
}

.card-img-top {
    height: 200px;
    object-fit: cover;
}
</style>
