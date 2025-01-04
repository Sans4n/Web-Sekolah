<template>
  <div class="container mt-4">
    <div class="text-center mb-4">
      <h1>Daftar Guru</h1>
      <p class="text-muted">SMK Negeri 4 Tasikmalaya</p>
    </div>
    <div class="row">
      <div class="col-md-3 mb-4" v-for="teacher in teachers" :key="teacher.id">
        <div class="card shadow-sm">
          <img :src="teacher.image" alt="Guru" class="card-img-top" />
          <div class="card-body">
            <h5 class="card-title">{{ teacher.name }}</h5>
            <p class="card-text">{{ teacher.subject }}</p>
          </div>
        </div>
      </div>
    </div>
    <div class="text-center py-5">
      <button class="btn btn-primary" @click="loadMore" :disabled="allLoaded">
        {{ allLoaded ? 'Semua Data Dimuat' : 'Muat Lebih Banyak' }}
      </button>
    </div>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';


const db_teachers = ref([
  { id: 1, name: 'Taufik Hidayat, S.Kom.', subject: 'Math', image: new URL('@/assets/img/Taufik.jpg', import.meta.url).href },
  { id: 2, name: 'Zul Hilmi, S.T.', subject: 'English', image: new URL('@/assets/img/Zul.jpg', import.meta.url).href },
  { id: 3, name: 'Deni Maulana, S.T.', subject: 'Science', image: new URL('@/assets/img/Deni.jpg', import.meta.url).href },
  { id: 4, name: 'Arip, S.T., M.Kom.', subject: 'History', image: new URL('@/assets/img/Arip.jpg', import.meta.url).href },
  { id: 5, name: 'Adi Iasan, S.T.', subject: 'Physics', image: new URL('@/assets/img/Adi.jpg', import.meta.url).href },
  { id: 6, name: 'Andi Moh Permadi, S.Kom.', subject: 'Chemistry', image: new URL('@/assets/img/Andi.jpg', import.meta.url).href },
  { id: 7, name: 'Bintang Anugrahing Widhi, S.T.', subject: 'Biology', image: new URL('@/assets/img/Bintang.jpg', import.meta.url).href },
  { id: 8, name: 'Lisye Diana Inggriani, S.Kom.', subject: 'Geography', image: new URL('@/assets/img/Lisye.jpg', import.meta.url).href },
  { id: 9, name: 'Imas Masruroh, S.T.', subject: 'Sport', image: new URL('@/assets/img/Imas.jpg', import.meta.url).href },
  { id: 10, name: 'Suminar, M.Kom.', subject: 'Art', image: new URL('@/assets/img/Suminar.jpg', import.meta.url).href },
  { id: 11, name: 'Lisna Windi Nurhuda, S.Pd.', subject: 'Sport', image: new URL('@/assets/img/Lisna.jpg', import.meta.url).href },
  { id: 12, name: 'Hj. Sri Agustina, S.Pd., M.Pd.', subject: 'Art', image: new URL('@/assets/img/Sri.jpg', import.meta.url).href },
]);


const teachers = ref([...db_teachers.value.slice(0, 4)]);

const limitStart = ref(teachers.value.length);
const limitEnd = ref(limitStart.value + 4);


const loadMore = () => {
  teachers.value = [...teachers.value, ...db_teachers.value.slice(limitStart.value, limitEnd.value)];
  limitStart.value = limitEnd.value;
  limitEnd.value += 4;
};


const allLoaded = computed(() => limitStart.value >= db_teachers.value.length);
</script>

<style scoped>

.card {
  border-radius: 10px;
}

.card-img-top {
  height: 150px;
  object-fit: cover;
}
</style>
