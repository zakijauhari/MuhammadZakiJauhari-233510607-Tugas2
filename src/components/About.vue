<template>
  <section id="about" class="about section">
    <div class="container">
      <h2>Tentang Saya</h2>
      <div class="about-content">
        <div class="about-text">
          <p>Halo! Saya Muhammad Zaki Jauhari, lahir di Pekanbaru pada tanggal 5 Januari 2004. Saya adalah seorang pengembang web yang bersemangat dengan keahlian di bidang teknologi frontend, memiliki ketertarikan pada desain, dan gemar dalam pengelolaan database.</p>
          <p>Perjalanan saya dalam pengembangan web dimulai ketika saya menemukan kekuatan untuk menciptakan pengalaman digital yang digunakan oleh banyak orang setiap hari. Sejak saat itu, saya berdedikasi untuk membuat aplikasi yang bersih, efisien, dan mudah digunakan.</p>
          <p>Selain coding, saya juga terampil dalam berbicara di depan umum dan kepemimpinan. Saya memiliki hak istimewa untuk memimpin sebuah komunitas besar, yang telah mengasah keterampilan komunikasi dan organisasi saya.</p>
          <p>Ketika saya tidak sedang membuat program, Anda bisa menemukan saya sedang menjelajahi tren desain baru, berkontribusi pada proyek open-source, atau membimbing para pengembang yang bercita-cita tinggi.</p>
        </div>
        <div class="about-details">
          <div class="detail-card">
            <h3>Pendidikan</h3>
            <p>SD Negeri 114 Pekanbaru (2010-2016)</p>
            <p>SMP Negeri 32 Pekanbaru (2016-2019)</p>
            <p>SMA Negeri 9 Pekanbaru (2019-2022)</p>
            <p>Universitas Islam Riau (2023-Sekarang)</p>
          </div>
          <div class="detail-card">
            <h3>Pencapaian</h3>
            <p>Juara 1 Lomba Syair se-Kecamatan Pekanbaru Kota (2014)</p>
            <p>Juara 1 Lomba Tilawah Quran se-Kelurahan Tanah Datar (2019)</p>
            <p>Juara 3 Lomba Tilawah Quran se-Kecamatan Pekanbaru Kota(2019)</p>
            <p>Juara 2 Lomba Tilawah Quran se-Kelurahan Tanah Datar (2020)</p>
            <p>Juara 1 Lomba Tilawah Quran se-Kelurahan Tanah Datar (2021)</p>
            <p>Harapan 3 Lomba Tilawah Quran se-Kecamatan Pekanbaru Kota (2021)</p>
            <p>Juara 3 Tournament Arisan King Billiard Pool & Caffe (2021)</p>
            <p>Juara 2 Lomba Tilawah Quran se-Kelurahan Tanah Datar (2022)</p>
            <p>The Most Handsome SMA Negeri 9 Pekanbaru (2022)</p>
            <p>Juara 2 Lomba Tilawah Quran se-Kelurahan Tanah Datar (2023)</p>
          </div>
          <div class="detail-card">
            <h3>Kepemimpinan</h3>
            <p>Kepala Divisi Hubungan Masyarakat Tim Supporter Curvanord 1955 Distrik Brigata Nord Sukajadi Laferza (2019)</p>
            <p>Ketua Komunitas PNC (2022)</p>
            
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'About'
}
</script>

<style scoped>
.about-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 3rem;
  align-items: start;
}

.about-text {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.about-details {
  display: grid;
  grid-template-columns: 1fr;
  gap: 1.5rem;
}

.detail-card {
  background-color: var(--bg-secondary);
  padding: 2rem;
  border-radius: 10px;
  box-shadow: var(--shadow);
  transition: var(--transition);
}

.detail-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
}

.detail-card h3 {
  color: var(--primary-color);
  margin-bottom: 0.5rem;
}

.detail-card p {
  margin-bottom: 0.5rem;
}

@media (max-width: 768px) {
  .about-content {
    grid-template-columns: 1fr;
  }
}
</style>