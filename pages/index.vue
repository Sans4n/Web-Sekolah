<template>
  <div id="carouselExample" class="carousel slide" data-bs-ride="carousel" data-bs-interval="2500">
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img src="@/assets/img/smk4.png" class="d-block w-100 img-overlay" alt="Slide 1" />
        <div class="carousel-caption">
          <h3>Selamat Datang di SMKN 4 Tasikmalaya</h3>
          <p>Generasi unggul dan berprestasi</p>
        </div>
      </div>
      <div class="carousel-item">
        <img src="@/assets/img/foto4.png" class="d-block w-100 img-overlay" alt="Slide 2" />
        <div class="carousel-caption">
          <h3>Fasilitas Modern</h3>
          <p>Kenyamanan belajar dengan fasilitas lengkap</p>
        </div>
      </div>
      <div class="carousel-item">
        <img src="@/assets/img/foto3.png" class="d-block w-100 img-overlay" alt="Slide 3" />
        <div class="carousel-caption">
          <h3>Kompetensi Terbaik</h3>
          <p>Mempersiapkan siswa untuk masa depan</p>
        </div>
      </div>
    </div>
    <button class="carousel-control-prev" type="button" data-bs-target="#carouselExample" data-bs-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#carouselExample" data-bs-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>
  <div class="container-fluid my-5">
    <div class="row justify-content-center">
      <div class="col-md-4 text-center">
        <img src="@/assets/img/kepsek.png" alt="Foto Kepala Sekolah" class="img-fluid rounded-circle mb-3">
        <h3>Kurniawan, S.Pd, M.Pd.</h3>
        <p><em>Kepala Sekolah SMK Negeri 4 Tasikmalaya</em></p>
      </div>
      <div class="col-md-8 pt-4">
        <div class="card">
          <div class="card-body">
            <h1 class="pb-3">Sambutan Kepala Sekolah</h1>
            <p>
              Assalamu’alaikum warahmatullahi wabarakatuh. <br>
              Salam sejahtera bagi kita semua.
            </p>
            <p>
              Puji syukur kita panjatkan ke hadirat Allah SWT atas rahmat dan karunia-Nya sehingga kita dapat berkumpul
              dalam keadaan sehat wal afiat.
              Pendidikan adalah fondasi penting dalam membangun generasi bangsa yang cerdas, berkarakter, dan berdaya
              saing. Kami di SMK Negeri 4 Tasikmalaya berkomitmen untuk memberikan pendidikan terbaik bagi siswa-siswi
              kami.
            </p>
            <p>
              Semoga website ini dapat menjadi sarana informasi, komunikasi, dan inspirasi bagi seluruh warga sekolah
              dan masyarakat. Terima kasih atas dukungan dan partisipasi semua pihak.
            </p>
            <p>
              Wassalamu’alaikum warahmatullahi wabarakatuh.
            </p>
            <p class="text-end"><strong>- Kurniawan, S.Pd, M.Pd.</strong></p>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="info-section text-center">
    <h2>Guru, Staf dan Peserta Didik</h2>
    <p>Tahun Pelajaran 2023/2024</p>
    <div class="container-fluid mt-4">
      <div class="row">
        <div class="col-md-4">
          <div class="info-box">
            <i class="bi bi-person-video3" style="font-size: 2rem;"></i>
            <h4>60</h4>
            <p>Guru</p>
          </div>
        </div>
        <div class="col-md-4">
          <div class="info-box">
            <i class="bi bi-people" style="font-size: 2rem;"></i>
            <h4>10</h4>
            <p>Staf</p>
          </div>
        </div>
        <div class="col-md-4">
          <div class="info-box">
            <i class="bi bi-mortarboard" style="font-size: 2rem;"></i>
            <h4>1,470</h4>
            <p>Peserta Didik</p>
          </div>
        </div>
      </div>
    </div>
  </div>
  <section id="about" class="">
    <div class="card pb-5" style="max-width: 100%;">
      <div class="row g-0">
        <div class="col-md-8 pt-5">
          <div class="card-body">
            <h2 class="about card-title text-center pt-5">Tentang SMK NEGERI 4 TASIKMALAYA</h2>
            <p class="card-text">Sejalan dengan Program Pemerintah dibidang pendidikan Menengah Kejuruan pada saat itu
              yakni pemerataan akses ditambah pula dengan banyaknya keinginan masyarakat yang mengharapkan adanya SMK
              Negeri di daerah Kecamatan Purbaratu Kota Tasikmalaya, terutama untuk menampung tamatan dari SLTP yang
              ingin melanjutkan ke SMK maka beberapa tokoh masyarakat, unsur pejabat pemerintah di Kecamatan Purbaratu
              Kota Tasikmalaya mengusulkan kepada pemerintah Kota Tasikmalaya dan Pemerintah Provinsi Jawa Barat, agar
              berdirinya SMK Negeri di Kecamatan Purbaratu Kota Tasikmalaya.</p>
            <p class="card-text"><small class="text-muted">lebih lanjut</small></p>
          </div>
        </div>
        <div class="col-md-4">
          <img src="@/assets/img/Logo-SMK.png" class="img-fluid  p-4 " alt="...">
        </div>
      </div>
    </div>
  </section>

  <div class="container-fluid bg-success text-white bg-opacity-75 py-5">
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
  { src: foto1, title: "Upacara 17 Agustus" },
  { src: foto2, title: "Upacara 17 Agustus" },
  { src: foto3, title: "Upacara 17 Agustus" },
  { src: foto4, title: "Foto Bersama" },
  { src: foto5, title: "Foto Bersama" },
  { src: foto6, title: "MPLS" },
])

</script>
<style scoped>
.img-overlay {
  opacity: 75%;
  object-fit: cover;
}

/* Mengatur tinggi maksimal gambar carousel */
.carousel-inner img {
  max-height: 70vh;
}

/* Styling untuk teks overlay */
.carousel-caption {
  position: absolute;
  bottom: 20%;
  left: 50%;
  transform: translateX(-50%);
  color: white;
  text-align: center;
  padding: 15px 20px;
  border-radius: 10px;
}

.carousel-caption h3 {
  font-size: 2rem;
  font-weight: bold;
  margin-bottom: 10px;
}

.carousel-caption p {
  font-size: 1.2rem;
}

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

.info-section {
  background-color: rgb(0, 138, 94);
  /* Warna latar belakang gelap */
  color: white;
  /* Teks warna putih */
  padding: 40px 20px;
}

.info-box {
  background-color: #50a782;
  /* Warna kotak */
  padding: 20px;
  border-radius: 8px;
  text-align: center;
  color: #ffffff;
  /* Warna ikon */
}

.info-box h4 {
  color: white;
  /* Warna teks angka */
  margin-top: 10px;
}

.info-box p {
  margin: 0;
  font-size: 14px;
}
</style>