<template>
  <transition name="fade" appear>
    <main>
      <!-- a wrapper for slot is needed -->
      <div class="grey lighten-5">
        <Layout>
          <Hero />
          <!-- Intro section -->
          <div class="how-section spad set-bg">
            <div class="container text-white">
              <div class="row">
                <div class="col-xs-6">
                  <div class="section-title">
                    <h2>Profil Desa</h2>
                  </div>
                </div>
                  <p align='justify'><b>
                    Sebelum adanya pemekaran Desa yang menjadi induk adalah Desa Tambun 
                    Sukadami kemudian pada Tahun 1978 terjadi pemekaran Desa yaitu menjadi 
                    2 (dua) Desa yaitu Desa Tambun Suka Dami dan Desa Lambang Jaya dan pada 
                    tahun 1983 Desa Tambun Suka Dami kembali dipecah menjadi 3 (tiga) Desa 
                    yaitu Desa Setia Darma Desa Mekar Sari dan Induknya Menjadi Desa Tambun.
                    </b>
                  </p>

                  <p align='justify'><b>
                    Desa Tambun di tinjau dari pembagian wilayah administrasi termasuk dalam 
                    wilayah Kecamatan Tambun Selatan Kabupaten Bekasi Propinsi Jawa Barat. Adapun 
                    jarak dari Desa Tambun ke Kecamatan ± 100 m, jarak ke Kota Kabupaten ± 14 Km, 
                    jarak ke Ibu Kota Propinsi Jawa Barat ± 120 Km dan jarak dengan Ibu Kota Negara 
                    Republik Indonesia ± 35 Km. 
                    </b>
                  </p>

                  <p align='justify'><b>
                    Perkembangan penduduk senantiasa ditentukan oleh faktor kelahiran, kematian, 
                    pindah dan datang. Hal ini dapat berubah dari bulan ke bulan. Adapun jumlah 
                    penduduk Desa Tambun Kecamatan Tambun Selatan sampai akhir April 2014 tercatat 
                    19.205 jiwa 
                    </b>
                  </p>
              </div>
            </div>
          </div>

          <div v-if="covid !== null">
            <div class="concept-section spad set-bg">
            <div class="container">
                <div class="row">
                  <div class="col-lg-9">
                    <div class="section-title">
                      <h2>Pantauan Data Covid-19</h2>
                      <h1> Nasional </h1>
                    </div>
                  </div>
                </div>
                <div class="row">
                  <div class="col-lg-3">
                    <div class="premium-item">
                      <h5>Terkonfirmasi</h5>
                      <div id="konfirm_nasional">
                        <h1>{{ covid.confirmed.value }}</h1>
                      </div>
                    </div>
                  </div>

                  <div class="col-lg-3">
                    <div class="premium-item">
                      <h5>Sembuh</h5>
                      <div id="sembuh_nasional">
                        <h1>{{ covid.recovered.value }}</h1>
                      </div>
                    </div>
                  </div>
                  <div class="col-lg-3">
                    <div class="premium-item">
                      <h5>Meninggal</h5>
                      <div id="meninggal_nasional">
                        <h1>{{ covid.deaths.value }}</h1>
                      </div>
                    </div>
                  </div>

                  <div class="col-lg-3">
                    <div class="premium-item">
                      <h5>Terkahir Update:</h5>
                      <div id="last_update">
                        <h2>{{ covid.lastUpdate }}</h2>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <div class="how-section spad">
            <div class="container text-white">
                  <div class="section-title">
                    <h2>Peta Sebaran Covid-19</h2>
                    <h1> Kabupaten Bekasi</h1>
                  </div>
                  <div style="text-align: center;">
                  <iframe
                  src="https://www.google.com/maps/d/embed?mid=1H2P_ASpqbQP3MNJf7xPMo7AWEL0z6Fk4" 
                  width="1200" height="480">
                  </iframe>
                  </div>
            </div>
          </div>


          <!-- How section -->
          <div class="concept-section spad set-bg">
            <div class="container">
              <div class="row">
                <div class="col-lg-6">
                  <div class="section-title">
                    <h2>Program Kerja</h2>
                  </div>
                </div>
              </div>
              <div class="row">
                <div class="col-lg-3 col-sm-6">
                  <div class="concept-item">
                    <g-link to="/blog/penanaman-bibit/">
                      <g-image src="../assets/menanam.jpg" />
                    </g-link>
                    <h5>Penanaman Bibit</h5>
                  </div>
                </div>
                <div class="col-lg-3 col-sm-6">
                  <div class="concept-item">
                    <g-link to="/blog/edukasi-covid-burhat-dan-maseco/">
                      <g-image src="../assets/instalasi.jpg" />
                    </g-link>
                    <h5>Pembuatan Fasilitas Kesehatan</h5>
                  </div>
                </div>
                <div class="col-lg-3 col-sm-6">
                  <div class="concept-item">
                    <g-link to="/blog/olahan-makanan-tempe/">
                      <g-image src="../assets/masak.jpg" />
                    </g-link>
                    <h5>Inovasi Olahan Tempe</h5>
                  </div>
                </div>
                <div class="col-lg-3 col-sm-6">
                  <div class="concept-item">
                    <g-link to="/blog/pembagian-handsanitizer/">
                      <g-image src="../assets/hand.jpg" />
                    </g-link>
                    <h5>Pembagian Hand Sanitizer</h5>
                  </div>
                </div>
              </div>
            </div>
          </div>

           <div class="how-section spad">
            <div class="container text-white">
                  <div class="section-title">
                    <h2>Tentang Covid-19</h2>
                  </div>
                  <p align='justify'>
                    Coronavirus Disease 2019 atau Covid-19 adalah
                    <b
                      >penyakit baru yang dapat menyebabkan gangguan pernapasan
                      dan radang paru</b
                    >. Penyakit ini disebabkan oleh infeksi
                    <i
                      >Severe Acute Respiratory Syndrome Coronavirus 2
                      (SARS-CoV-2)</i
                    >. Gejala klinis yang muncul beragam, mulai dari seperti
                    <b
                      >gejala flu biasa (batuk, pilek, nyeri tenggorok, nyeri
                      otot, nyeri kepala) sampai yang berkomplikasi berat
                      (pneumonia atau sepsis).</b
                    >
                  </p>

                  <p align='justify'>
                    Covid-19 adalah penyakit baru dan para peneliti masih
                    mempelajari bagaimana cara penularannya. Dari berbagai
                    penelitian,
                    <b
                      >metode penyebaran utama penyakit ini diduga adalah
                      melalui droplet saluran pernapasan dan kontak dekat dengan
                      penderita</b
                    >.
                    <b
                      >Droplet merupakan partikel kecil dari mulut penderita
                      yang dapat mengandung virus</b
                    >
                    penyakit, yang dihasilkan pada saat batuk, bersin, atau
                    berbicara. Droplet dapat melewati sampai jarak tertentu
                    (biasanya 1 meter).
                  </p>

                  <p align='justify'>
                    <b
                      >Droplet bisa menempel di pakaian atau benda di sekitar
                      penderita</b
                    >
                    pada saat batuk atau bersin. Namun, partikel droplet cukup
                    besar sehingga tidak akan bertahan atau mengendap di udara
                    dalam waktu yang lama. Namun,
                    <b
                      >masyarakat diwajibkan untuk menggunakan masker kain yang
                      menutupi hidung dan mulut</b
                    >
                    untuk mencegah penyebaran droplet.
                  </p>
            </div>
          </div>
          
          <!-- concept section -->
          <div class="concept-section spad">
            <div class="container">
              <div class="row">
                <div class="section-title">
                    <h2>Layanan Darurat Covid-19</h2>
                  </div>
                <div class="col-lg-6">
                  <ol class="sub-list">
                    <li>Anda mengalami gejala Covid-19</li>
                    <li>
                      Anda baru-baru ini berkunjung ke suatu negara atau daerah
                      dengan risiko tinggi coronavirus
                    </li>
                    <li>
                      Anda telah melakukan kontak dekat dengan seseorang dengan
                      coronavirus
                    </li>
                  </ol>
                </div>
                <div class="col-lg-6">
                  <h3>Hubungi layanan ini jika:</h3>
                  <div class="hs-text">
                    <p>
                      <a href="tel:112" class="site-btn"
                        >Layanan Call Center <b>112/119</b> (BEBAS PULSA / TOLL
                        FREE)</a
                      >
                    </p>
                    <p>
                      <a href="tel:08111139927" class="site-btn"
                        >Dinas Kesehatan Kabupaten Bekasi (<b>08111139927</b>)</a
                      >
                    </p>
                    <p>
                      <a href="https://pikokabsi.bekasikab.go.id/" class="site-btn sb-c2">Kontak Selengkapnya</a>
                    </p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </Layout>
      </div>
    </main>
  </transition>
</template>

<script>
import Navbar from "../components/navbar";
import Hero from "../components/hero";
import CegahCovid from "../components/cegahcovid";
import axios from "axios";
export default {
  components: {
    Navbar,
    Hero,
    CegahCovid
  },
  metaInfo: {
    title: "Desa Tambun"
  },
  data() {
    return {
      covid: null
    };
  },
  mounted() {
    axios.get("https://covid19.mathdro.id/api/countries/IDN").then(res => {
      console.log(res.data);
      this.covid = res.data;
    });
  }
};

</script>
<style scoped>
p {
  font-size: 16px;
}

.home-banner {
  background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
    url("../assets/kantor.jpg");
  background-size: cover;
  background-position: center;
  height: 500px;
  width: 100%;
  display: flex;
  align-items: center;
}

.fade-enter-active {
  transition: opacity 0.5s;
}

.fade-enter {
  opacity: 0;
}

iframe {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 100%;
}
</style>

