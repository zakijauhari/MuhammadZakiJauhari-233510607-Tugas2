<template>
  <section id="projects" class="projects section">
    <div class="container">
      <h2 class="section-title">Proyek Saya</h2>
      <div class="projects-grid">
        <div class="project-card" v-for="(project, index) in projects" :key="index">
          <div class="project-image">
            <img :src="project.imageUrl" :alt="project.title" class="project-img">
            <div class="project-overlay">
              <div class="project-links">
                <a :href="project.demo" target="_blank" class="demo-btn">Live Demo</a>
                <a :href="project.code" target="_blank" class="code-btn">View Code</a>
              </div>
            </div>
          </div>
          <div class="project-content">
            <h3 class="project-title">{{ project.title }}</h3>
            <p class="project-desc">{{ project.description }}</p>
            <div class="project-tech">
              <span v-for="(tech, i) in project.technologies" :key="i" class="tech-tag">{{ tech }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Projects',
  data() {
    return {
      projects: [
        {
          title: 'Legacy Story Our Relationship',
          description: 'Sebuah website tentang legacy cinta yang abadi diantara saya dan kekasih.',
          technologies: ['HTML', 'CSS', 'JavaScript'],
          imageUrl: `${import.meta.env.BASE_URL}images/foto1.png`,
          demo: 'https://zakijauhari.github.io/legacy-of-our-story/',
          code: 'https://github.com/zakijauhari/legacy-of-our-story.git'
        },
        {
          title: 'Aplikasi Manajemen Tugas (To Do List)',
          description: 'Aplikasi untuk mengelola jurnal kegiatan harian.',
          technologies: ['Vue.js', 'CSS', 'SQLYog'],
          imageUrl: `${import.meta.env.BASE_URL}images/foto2.png`,
          demo: 'https://zakijauhari.github.io/32-pbk-uts-233510607/',
          code: 'https://github.com/zakijauhari/32-pbk-uts-233510607.git'
        },
        {
          title: 'Aplikasi Inventory',
          description: 'Aplikasi untuk mengelola inventory barang.',
          technologies: ['Vue.js', 'CSS', 'SQLYog'],
          imageUrl: `${import.meta.env.BASE_URL}images/foto3.png`,
          demo: 'https://zakijauhari.github.io/Tugas-PBK-P10/',
          code: 'https://github.com/zakijauhari/Tugas-PBK-P10.git'
        }
      ]
    }
  }
}
</script>

<style scoped>
.projects.section {
  padding: 4rem 0;
  background-color: var(--bg-primary);
  
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 1rem;
}

.section-title {
  text-align: center;
  font-size: 2.5rem;
  margin-bottom: 3rem;
  color: var(--heading-color);
  transition: color 0.3s ease;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
  gap: 2.5rem;
}

.project-card {
  background-color: var(--bg-secondary);
  border-radius: 12px;
  overflow: hidden;
  box-shadow: var(--shadow);
  border: 1px solid var(--border-color);
  
}

.project-card:hover {
  transform: translateY(-10px);
  box-shadow: var(--card-hover-shadow);
}

.project-image {
  position: relative;
  height: 220px;
  overflow: hidden;
}

.project-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.5s ease;
}

.project-card:hover .project-img {
  transform: scale(1.05);
}

.project-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.7);
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.project-card:hover .project-overlay {
  opacity: 1;
}

.project-links {
  display: flex;
  gap: 1rem;
  
}

.demo-btn, .code-btn {
  padding: 0.8rem 1.5rem;
  border-radius: 30px;
  font-weight: 600;
  transition: all 0.3s ease;
  text-decoration: none;
}

.demo-btn {
  background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
  color: white;
}

.demo-btn:hover {
  transform: translateY(-2px);
  opacity: 0.9;
}

.code-btn {
  background: transparent;
  color: white;
  border: 2px solid white;
}

.code-btn:hover {
  background: rgba(255, 255, 255, 0.1);
  transform: translateY(-2px);
}

.project-content {
  padding: 1.5rem;
}

.project-title {
  font-size: 1.4rem;
  margin-bottom: 0.75rem;
  color: var(--heading-color);
}

.project-desc {
  color: var(--text-secondary);
  font-size: 0.95rem;
  line-height: 1.6;
  margin-bottom: 1.25rem;
}

.project-tech {
  display: flex;
  flex-wrap: wrap;
  gap: 0.6rem;
}

.tech-tag {
  background-color: var(--bg-primary);
  
  color: var(--tech-tag-text);
  padding: 0.4rem 0.9rem;
  border-radius: 20px;
  font-size: 0.8rem;
  font-weight: 500;
  transition: all 0.3s ease;
  border: 1px solid var(--tech-tag-border);
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
}

.tech-tag:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

@media (max-width: 768px) {
  .projects-grid {
    grid-template-columns: 1fr;
  }
  
  .section-title {
    font-size: 2rem;
  }
}
</style>