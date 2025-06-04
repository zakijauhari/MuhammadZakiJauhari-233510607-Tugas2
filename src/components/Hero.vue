<template>
  <section id="home" class="hero section">
    <div class="container">
      <div class="hero-content">
        <div class="hero-text slide-up">
          <h1>Zaki Jauhari</h1>
          <h2>Pengembang Web | UI/UX Antusias | Manajemen Database | Pemograman Algoritma | DevOps | Deployment | Soft Skills</h2>
          <p>“Sebuah teknologi yang estetis menciptakan pengalaman, bukan hanya solusi.”</p>
          <div class="hero-buttons">
            <a href="#contact" class="btn">Hubungi Saya</a>
            <a href="#projects" class="btn btn-outline">Projek Saya</a>
          </div>
        </div>
        <div class="hero-image fade-in">
          <div class="image-wrapper">
            <img src="../assets/profil.jpg" alt="Muhammad Zaki Jauhari" class="profile-img">
            <div class="glow"></div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Hero'
}
</script>

<style scoped>
.hero {
  min-height: 100vh;
  display: flex;
  align-items: center;
  padding-top: 80px;
}

.hero-content {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 3rem;
}

.hero-text {
  flex: 1;
}

.hero-text h1 {
  font-size: 3.5rem;
  margin-bottom: 1.5rem;
  background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
}

.hero-text h2 {
  font-size: 1.8rem;
  font-weight: 500;
  color: var(--text-secondary);
  margin-bottom: 2rem;
}

.hero-text p {
  font-size: 1.2rem;
  max-width: 600px;
  margin-bottom: 2.5rem;
}

.hero-buttons {
  display: flex;
  gap: 1rem;
}

.hero-image {
  flex: 1;
  display: flex;
  justify-content: center;
}

.image-wrapper {
  position: relative;
  width: 350px;
  height: 350px;
  border-radius: 50%;
  overflow: hidden;
}

.profile-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 50%;
  position: relative;
  z-index: 2;
}

.glow {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border-radius: 50%;
  background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
  filter: blur(20px);
  opacity: 0.5;
  z-index: 1;
  animation: pulse 4s infinite;
}

@media (max-width: 992px) {
  .hero-content {
    flex-direction: column-reverse;
    text-align: center;
  }
  
  .hero-buttons {
    justify-content: center;
  }
  
  .image-wrapper {
    width: 250px;
    height: 250px;
  }
}

@media (max-width: 576px) {
  .hero-text h1 {
    font-size: 2.5rem;
  }
  
  .hero-text h2 {
    font-size: 1.5rem;
  }
  
  .hero-buttons {
    flex-direction: column;
    align-items: center;
  }
}
</style>