<template>
  <div class="container-fluid">
    <div class="row p-3 bg-success text-white align-items-center">
      <div class="col-4 col-lg-1 text-center">
        <img src="../assets/img/Logo-SMK.png" alt="Logo SMKN 4 Tasikmalaya" class="img-fluid rounded">
      </div>
      <div class="col-8 col-lg-11">
        <h1 class="mb-0">SMKN 4 Tasikmalaya</h1>
        <address class="mb-0">
          Jl. Depok, Sukamenak, Purbaratu
        </address>
      </div>
    </div>
    
    <div class="row p-1 bg-success text-white bg-opacity-75">
      <div class="col-12">
        <ul class="d-flex list-unstyled mb-0 menu justify-content-center">
          <li class="me-3">
            <NuxtLink to="/" class="nav-link text-white">Home</NuxtLink>
          </li>
          <li class="me-3 dropdown">
            <a href="#" class="btn text-white p-2 dropdown-toggle">Profil</a>
            <ul class="dropdown-menu">
              <li><NuxtLink to="/sejarah" class="dropdown-item">Sejarah</NuxtLink></li>
              <li><NuxtLink to="/profil" class="dropdown-item">Identitas Sekolah</NuxtLink></li>
              <li><NuxtLink to="/visimisi" class="dropdown-item">Visi dan Misi</NuxtLink></li>
              <li><NuxtLink to="/galeri" class="dropdown-item">Galeri</NuxtLink></li>
            </ul>
          </li>
          <li class="me-3">
            <NuxtLink to="/guru" class="nav-link text-white">Guru</NuxtLink>
          </li>
          <li class="me-3">
            <NuxtLink to="/berita" class="nav-link text-white">Berita</NuxtLink>
          </li>
          <li class="me-3">
            <NuxtLink to="/fasilitas" class="nav-link text-white">Fasilitas</NuxtLink>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style>
  
  .row {
    flex-wrap: wrap;
  }

  .dropdown-menu {
    margin-top: 0;
    padding: 0;
    display: none;
    position: absolute;
  }

  .d-flex {
    display: flex;
    align-items: center;
  }

  img {
    max-width: 100%;
    height: auto;
  }

  .nav-link {
    padding: 7px 20px;
  }

  .nav-link:hover {
    background-color:rgb(0, 138, 94);
    color: white;
    border-radius: 5px;
  }

  .dropdown-menu .dropdown-item:hover {
    background-color:rgb(0, 138, 94);
    color: white;
  }

  .dropdown-toggle:hover {
    background-color:rgb(0, 138, 94);
    color: white;
  }

  .dropdown:hover .dropdown-menu {
    display: block;
  }

  .dropdown {
    position: relative;
  }

  
  @media (max-width: 991px) {
    .col-lg-1 {
      text-align: center;
      margin-bottom: 1rem;
    }
    .col-lg-11 {
      text-align: center;
    }

    
    .menu {
      justify-content: flex-end;
      flex-wrap: wrap;
    }

    .menu li {
      margin-bottom: 10px;
    }

    .dropdown-menu {
      position: static;
      width: 100%;
      padding-left: 0;
      display: none;
    }

    .dropdown-menu .dropdown-item {
      display: block;
      width: 100%;
    }

    .dropdown:hover .dropdown-menu {
      display: block;
    }
  }

  @media (max-width: 576px) {
    .nav-link {
      padding: 7px 10px;
    }
  }
</style>