<template>
  <div>
    <header class="header-section clearfix d-none d-md-block">
      <g-link to="/" class="site-logo">
        <g-image src="../assets/logo.png" alt style="max-width:80px;" />
      </g-link>
      <g-link to="/" class="site-logo">
        <g-image src="../assets/logokkn.png" alt style="max-width:82px;" />
      </g-link>

      <ul class="main-menu">
        <li>
          <g-link to="/">Beranda</g-link>
        </li>
        <li>
          <g-link to="/blog/profil-desa">Tentang Desa</g-link>
        </li>
        <li>
          <a href>Program Kerja</a>
          <ul class="sub-menu">
            <li>
              <g-link to="/blog/tambunku-hijau">Tambunku Hijau</g-link>
            </li>
            <li>
              <g-link to="/blog/pembagian-handsanitizer">Pembagian Hand Sanitizer</g-link>
            </li>
            <li>
              <g-link to="/blog/edukasi-covid-burhat-dan-maseco">Edukasi Covid-19</g-link>
            </li>
            <li>
              <g-link to="/blog/olahan-makanan-tempe">Olahan Makanan Tempe</g-link>
            </li>
          </ul>
        </li>
        <li>
          <a href="#">Informasi</a>
          <ul class="sub-menu">
            <li>
              <a href="https://pikokabsi.bekasikab.go.id/">Layanan Darurat Covid-19</a>
            </li>
            <li>
              <a href="#">Pedoman New Normal</a>
            </li>
            <li>
              <a href="/blog/rs-rujukan">Lokasi RS Rujukan</a>
            </li>
          </ul>
        </li>
        <li>
          <a href="/News">Kabar Desa</a>
        </li>
      </ul>
    </header>
    <b-navbar toggleable="lg" type="dark" variant="info" class="d-md-none bg-dark">
      <b-navbar-brand>
        <g-image src="../assets/logo.png" alt style="max-width:50px;" />
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item>
            <g-link to="/" class="white">Beranda</g-link>
          </b-nav-item>
          <b-nav-item>
            <g-link to="/blog/kkn-t-jelupang" class="white">KKN-T IPB</g-link>
          </b-nav-item>
          <b-nav-item>
            <g-link to="/blog/profil-desa" class="white">Tentang Desa</g-link>
          </b-nav-item>
        </b-navbar-nav>

        <b-navbar-nav>
          <b-nav-item-dropdown text="Program Kerja" right>
            <b-dropdown-item class="sub">
              <g-link to="/blog/tambunku-hijau" class="grey">Tambunku Hijau</g-link>
            </b-dropdown-item>
            <b-dropdown-item>
              <g-link to="/blog/edukasi-covid-burhat-dan-maseco" class="grey">Instalasi Kebersihan</g-link>
            </b-dropdown-item>
            <b-dropdown-item>
              <g-link to="/blog/olahan-makanan-tempe" class="grey">Olahan Tempe</g-link>
            </b-dropdown-item>
            <b-dropdown-item>
              <g-link to="/blog/pembagian-handsanitizer" class="grey">Pembagian Hand Sanitizer</g-link>
            </b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
        <b-navbar-nav>
          <b-nav-item-dropdown text="Informasi" right>
            <b-dropdown-item href="#">Layanan Darurat Covid</b-dropdown-item>
            <b-dropdown-item
              href="https://lawancovid19.tangerangselatankota.go.id/lapor"
            >Lapor Gejala Covid-19</b-dropdown-item>
            <b-dropdown-item href="#">Pedoman New Normal</b-dropdown-item>
            <b-dropdown-item href="/blog/rs-rujukan">Lokasi RS Rujukan</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
  <!-- <b-navbar toggleable="lg" type="dark" variant="info">
    <b-navbar-brand href="#">NavBar</b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
        <b-nav-item href="#">Link</b-nav-item>
      </b-navbar-nav>

      <b-navbar-nav>
        <b-nav-item-dropdown text="Lang" right>
          <b-dropdown-item href="#">EN</b-dropdown-item>
          <b-dropdown-item href="#">ES</b-dropdown-item>
          <b-dropdown-item href="#">RU</b-dropdown-item>
          <b-dropdown-item href="#">FA</b-dropdown-item>
        </b-nav-item-dropdown>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>-->
</template>

<script>
// import {
//   BNavbar,
//   BNavbarBrand,
//   BNavbarToggle,
//   BNavbarNav,
//   BNavItemDropdown,
//   BDropdownItem,
//   BCollapse
// } from "bootstrap-vue";
export default {
  name: "Navbar"
  // components: {
  //   BNavbar,
  //   BNavbarBrand,
  //   BNavbarToggle,
  //   BNavbarNav,
  //   BNavItemDropdown,
  //   BDropdownItem,
  //   BCollapse
  // }
};
</script>

<style scoped>
.white {
  color: white;
  text-decoration: none;
}

.grey {
  color: #263238;
  text-decoration: none;
}

.sub > a {
  color: grey;
  text-decoration: none;
}

a {
  text-decoration: none;
}
</style>
