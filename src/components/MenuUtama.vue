<template>
  <b-container fluid>
    <b-row>
      <b-button @click="showMenu = !showMenu" class="pencetan" size="sm"
        >toggle menu</b-button
      >
      <b-col cols="3" class="side-menu" :class="showMenu ? 'show' : 'hidden'">
        <img class="poto-profil mt-4" src="../assets/profil2.jpeg" alt="" />
        <div class="nama mt-3">Arya Firmansyah</div>
        <div id="ikon-sosmed" class="mt-3">
          <a
            href="https://twitter.com/elonmusk?ref_src=twsrc%5Egoogle%7Ctwcamp%5Eserp%7Ctwgr%5Eauthor"
          >
            <b-avatar icon="twitter" class="sosmed"></b-avatar>
          </a>
          <a href="https://web.facebook.com/arya.firmansyah.9461/">
            <b-avatar icon="facebook" class="sosmed"></b-avatar>
          </a>
          <a href="https://www.instagram.com/arayasannn/?hl=id">
            <b-avatar icon="instagram" class="sosmed"></b-avatar>
          </a>
          <a href="https://www.youtube.com/c/windahbasudara">
            <b-avatar icon="youtube" class="sosmed"></b-avatar>
          </a>
        </div>
        <b-container class="bungkus-navigasi mb-5">
          <div
            @click="index = 0"
            :class="index === 0 ? 'item-navigasi pilihan' : 'item-navigasi'"
          >
            <b-icon-house /> home
          </div>
          <div
            @click="index = 1"
            :class="index === 1 ? 'item-navigasi pilihan' : 'item-navigasi'"
          >
            <b-icon-person />about
          </div>
          <div
            @click="index = 2"
            :class="index === 2 ? 'item-navigasi pilihan' : 'item-navigasi'"
          >
            <b-icon-file-earmark />resume
          </div>
          <div
            @click="index = 3"
            :class="index === 3 ? 'item-navigasi pilihan' : 'item-navigasi'"
          >
            <b-icon-envelope />contact
          </div>
        </b-container>
      </b-col>
      <b-col v-if="index === 0" cols="9" class="main-menu">
        <div class="intro">
          Hello semua! Saya Arya Firmansyah,saya adalah pelamar kerja baru!
          Salam kenal dan semoga saya nyaman dan semangat bekerja di sini!
        </div>
      </b-col>
      <b-col v-else-if="index === 1" cols="9" class="intro1">
        <div class="samaintro1">
          <h1>about</h1>
          <p>
            Nama saya Arya Firmansyah umur saya 20 tahun saya ,pengalaman saya
            belajar coding saya dibimbing oleh guru saya pak andrawan
            erlangga,saya belajar frontend,saya belajar coding menggunakan
            windows,dan menggunakan aplikasi atau web jsfiddle,vuejs,nodejs,dan
            visual studio code,impian saya setelah bisa coding adalah bekerja di
            perusahaan yang dimana perusahaan itu membutuhkan saya. saya belajar
            tentang coding atau progamer sejak kelas 12 SMK sari ajakan teman
            saya yang sudah lebih lama belajar coding atau programing. sekian
            About dari saya jika ada salah kata mohon maaf sebesar besarnya.Saya
            arya firmansyah sekian terimakasih
          </p>
        </div>
      </b-col>
      <b-col v-else-if="index === 2" cols="9" class="intro2">
        <div class="samaintro2">
          <h1 class="DataPribadi">DATA PRIBADI</h1>
          <ul class="list-group">
            <li class="list-group-item">Nama : Arya Firmansyah</li>
            <li class="list-group-item">
              Alamat : Villa Bekasi Indah 2 Blok.J12 no.12 RT.02 RW.38
            </li>
            <li class="list-group-item">
              Tempat Tanggal Lahir : Klaten,06 April 2005
            </li>
            <li class="list-group-item">No.Telepon : 085775358201</li>
            <li class="list-group-item">Jenis Klamin : Laki Laki</li>
            <li class="list-group-item">Agama : Islam</li>
            <li class="list-group-item">Kewarganegaraan : Indonesia</li>
            <li class="list-group-item">Status : Belum Menikah</li>
            <li class="list-group-item">Pendidikan Terakhir : Lulus SMK</li>
          </ul>
        </div>
      </b-col>
      <b-col v-else-if="index === 3" cols="9" class="intro3">
        <div class="samaintro3">
          <h1 class="hubungiKami">HUBUNGI KAMI</h1>
          <ul>
            <div>No.Telepon : 085775358201</div>
            <div>g-mail : arayasan14@gmail.com</div>
          </ul>
        </div>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  name: "MenuUtama",
  data: function () {
    return {
      index: 0,
      showMenu: true,
    };
  },
};
</script>


<style scoped>
.side-menu {
  background-color: #0d1931;
  min-height: 100vh;
}
.main-menu {
  background-image: url("../assets/background.jpeg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}
.poto-profil {
  border-radius: 50%;
  width: 150px;
  height: 150px;
  border: #2a2e57 solid 7px;
  object-fit: cover;
  object-position: center;
}
.nama {
  color: white;
  font-size: 25px;
  font-weight: bolder;
}
.sosmed {
  background-color: #2a2e57;
  color: white;
  margin-right: 7px;
  margin-left: 7px;
  padding: 2px;
}
.sosmed:hover {
  color: #bb1919;
  padding: 0px;
}
.bungkus-navigasi {
  text-align: left;
  margin-top: 60px;
  color: white;
  font-weight: 500px;
  font-size: 25px;
  margin-left: -20px;
  width: 120%;
}
.item-navigasi {
  padding-top: 25px;
  padding-bottom: 25px;
  padding-left: 55px;
  margin-left: -20px;
  margin-right: -20px;
}
.item-navigasi:hover {
  background-color: #2a2e57;
  font-weight: 700;
}
.pilihan {
  background-color: #474955;
}
.intro {
  color: white;
  font-size: 25px;
  margin-top: 300px;
  text-shadow: 2px 2px #000000;
  font-weight: bold;
  font-style: italic;
}
.intro1 {
  background-image: url("../assets/Apa-Itu-Coding.webp");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}
.samaintro1 {
  font-size: 25px;
  text-shadow: 2px 2px #000000;
  color: rgb(255, 255, 255);
  font-weight: bold;
  font-style: italic;
  margin-top: 100px;
}
.intro2 {
  background-image: url("../assets/apaajalah.jpeg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}
.pencetan {
  position: absolute;
  top: 7px;
  left: 5px;
  max-width: 100px;
  z-index: 1;
  display: none;
}
.show {
  display: block;
}
.hidden {
  display: none;
}
.DataPribadi {
  margin-top: 15px;
}
.samaintro2 {
  margin-right: 300px;
  font-size: 20px;
  text-align: left;
}
.intro3 {
  background-image: url("../assets/apaajalah.jpeg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}
.samaintro3 {
  font-size: 25px;
}

@media (max-width: 500px) {
  .side-menu {
    position: absolute;
    width: 300px;
  }
  .main-menu {
    min-width: 100%;
    min-height: 800px;
  }
  .pencetan {
    display: block;
  }
}
</style>
