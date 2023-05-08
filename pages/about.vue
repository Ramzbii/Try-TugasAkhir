<template>
    <div class="about-page">
  <section class="page-header">
    <div class="page-header-description">
      <h2>SANTANU - Sistem Pemantauan Hujan</h2>
      <p>
        SANTANU adalah sistem monitoring untuk pemantauan hujan skala lokal
        sebagai teknologi alternatif untuk mengisi daerah-daerah yang tidak
        terpantau oleh radar cuaca yang sudah ada.
      </p>
      <p>
        SANTANU merupakan produk litbang Pusat Sains dan Teknologi Atmosfer
        LAPAN bekerjasama dengan PT. INTI untuk produksi dan komersialisasi,
        difasilitasi oleh Ristekdikti serta didukung oleh BMKG sebagai pembuat
        standar dan pengguna.
      </p>
    </div>
    <img src="../src/santanu-furuno.png" alt="radar-santanu" />
  </section>
  <section class="companies">
    <img src="../src/logo-brin.png" alt="Logo BRIN" />
    <img src="../src/logo-lapan.png" alt="Logo LAPAN" />
    <img src="../src/logo-pt-inti.png" alt="Logo PT INTI" />
    <img src="../src/logo-bmkg.png" alt="Logo BMKG" />
  </section>
  <section class="feature">
    <div class="feature-location">
      <h3>Lokasi SANTANU</h3>
      <p>Daerah yang sudah terpasang radar SANTANU:</p>
      <ul>
        <!-- <li v-for="radar in dataLokasiRadar" :key="radar['radar_id']">
          <fa class="menu-icon" icon="map-pin" />
          <span>{{ radar['radar_name'] }}</span>
        </li> -->
      </ul>
    </div>
    <div class="contact-us">
      <h3>Kontak</h3>
      <address>
        <strong>KST Samaun Samadikun</strong><br />
        <span>Jalan Sangkuriang, Dago, Kecamatan Coblong</span><br />
        <span>Bandung, 40135</span><br />
        <!-- <abbr title="Telephone">Telepon:</abbr> (022) 6012602, 6037445<br /> -->
        <!-- Fax. (022) 6014998, 6037443<br /> -->
        <abbr title="Email">Email:</abbr>
        <a href="mailto: psta@lapan.go.id"> prima@brin.go.id</a>
      </address>
    </div>
  </section>
  <footer class="footer-about">&copy; 2022 - Badan Riset dan Inovasi Nasional</footer>
</div>
</template>


<style>
.about-page {
  background-color: #FCFAF9;
}

.page-header {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2rem;
  width: min(90%, 80rem);
  margin-inline: auto;
  padding: 3rem 0;
}

.page-header h2 {
  color: #107c5c;
}

.page-header-description h2 {
  line-height: 2.75rem;
  margin-bottom: 2rem;
}

.page-header-description p {
  line-height: 2rem;
}

.page-header-description p:first-of-type {
  margin-bottom: 1rem;
}

.page-header img {
  width: min(70%, 250px);
  border-radius: 8px;
  box-shadow: 0 0 12px rgba(0, 0, 0, 0.15);
}

.companies {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  justify-items: center;
  column-gap: 3rem;
  row-gap: 4rem;
  padding: 6rem 1.5rem;
  background-color: #E9FAE3;
}

.companies img {
  height: 70px;
}

.feature {
  display: flex;
  flex-direction: column;
  gap: 4rem;
  justify-content: space-around;
  padding: 3rem 2rem;
}

.feature h3 {
  color: #107c5c;
}

.feature-location h3 {
  margin-bottom: 2rem;
}

.feature-location p {
  line-height: 2rem;
  margin-bottom: 1.25rem;
}

.feature-location ul {
  list-style-type: none;
}

.feature-location ul li {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
  margin-bottom: 1rem;
}

.feature-location ul li:last-child {
  margin-bottom: 0;
}

.contact-us {
  display: flex;
  flex-direction: column;
}

.contact-us h3 {
  margin-bottom: 2rem;
}

.contact-us address {
  font-style: normal;
  line-height: 2rem;
}

.contact-us address a {
  text-decoration: none;
}

.contact-us address a:hover {
  color: #477dcf;
}

.footer-about {
  padding: 1rem 2rem;
  background-color: #E9FAE3;
  border-top: 2px solid rgba(0,0,0,.2);
}

@media (min-width: 450px) {
  .companies img {
    height: 90px;
  }
}

@media (min-width: 650px) {
  .page-header {
    flex-direction: row;
    gap: 5rem;
  }

  .feature {
    flex-direction: row;
  }
}

@media (min-width: 750px) {
  .companies {
    display: flex;
    justify-content: space-around;
  }
}
</style>