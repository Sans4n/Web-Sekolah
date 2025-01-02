<template>
     <div class="container-fluid py-5">
        <div class="section-title text-dark">
            <h2>Berita Terbaru</h2>
        </div>
        <div class="row row-cols-1 row-cols-md-2 row-cols-lg-3 g-4">
            <!-- Card 1 -->
            <div class="col">
                <div class="card">
                    <div class="card-body">
                        <h5 class="card-title">19 Desember 2024</h5>
                        <p class="card-text">Galeri Penerapan Pembelajaran Kecakapan Hidup dan Program...</p>
                        <a href="#" class="btn btn-success">Baca Selengkapnya</a>
                    </div>
                </div>
            </div>
            <!-- Card 2 -->
            <div class="col">
                <div class="card">
                    <div class="card-body">
                        <h5 class="card-title">16 Desember 2024</h5>
                        <p class="card-text">Peringatan HUT ke-67 SMAN 1 Teladan Yogyakarta...</p>
                        <a href="#" class="btn btn-success">Baca Selengkapnya</a>
                    </div>
                </div>
            </div>
            <!-- Card 3 -->
            <div class="col">
                <div class="card">
                    <div class="card-body">
                        <h5 class="card-title">25 November 2024</h5>
                        <p class="card-text">Peringatan Hari Guru ke-79 SMAN 1 Yogyakarta...</p>
                        <a href="#" class="btn btn-success">Baca Selengkapnya</a>
                    </div>
                </div>
            </div>
            <!-- Tambahkan kartu lain di sini -->
        </div>
        <div class="text-center mt-4">
            <a href="#" class="btn btn-success">Tampilkan Semua Berita</a>
        </div>
    </div>
</template>

<script setup>

</script>

<style scoped>
.container-fluid {
    background-color: #fafafa; /* Warna latar belakang biru gelap */
}
.card {
    background-color: #fff;
    color: #000;
}
.section-title {
    text-align: center;
    margin-bottom: 30px;
    font-size: 24px;
    font-weight: bold;
}
/* .btn-primary {
    background-color: #f39c12;
    border-color: #f39c12;
}
.btn-primary:hover {
    background-color: #d68910;
    border-color: #d68910;
} */
</style>