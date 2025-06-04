<template>
  <section id="skills" class="skills section">
    <div class="container">
      <h2>Keterampilan</h2>
      <div class="skills-grid">
        <div class="skill-category">
          <h3>Keterampilan Teknis</h3>
          <div class="skills-list">
            <div class="skill-item" v-for="(skill, index) in technicalSkills" :key="'tech-'+index">
              <div class="skill-info">
                <span class="skill-name">{{ skill.name }}</span>
                <span class="skill-level">{{ skill.level }}%</span>
              </div>
              <div class="skill-bar">
                <div class="skill-progress" :style="{width: skill.level + '%'}"></div>
              </div>
            </div>
          </div>
        </div>
        <div class="skill-category">
          <h3>Keterampilan Diri</h3>
          <div class="skills-list">
            <div class="skill-item" v-for="(skill, index) in softSkills" :key="'soft-'+index">
              <div class="skill-info">
                <span class="skill-name">{{ skill.name }}</span>
                <span class="skill-level">{{ skill.level }}%</span>
              </div>
              <div class="skill-bar">
                <div class="skill-progress" :style="{width: skill.level + '%'}"></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Skills',
  data() {
    return {
      technicalSkills: [
        { name: 'HTML/CSS', level: 95 },
        { name: 'JavaScript', level: 90 },
        { name: 'Vue.js', level: 85 },
        { name: 'Database Desain', level: 80 },
        { name: 'UI/UX Desain', level: 85 },
        { name: 'Pemecahan Masalah', level: 90 }
      ],
      softSkills: [
        { name: 'Public Speaking', level: 90 },
        { name: 'Kepemimpinan', level: 85 },
        { name: 'Kolaborasi Tim', level: 88 },
        { name: 'Komunikasi', level: 92 },
        { name: 'Manajemen Waktu', level: 87 },
        { name: 'Mentoring/Pendampingan', level: 83 }
      ]
    }
  }
}
</script>

<style scoped>
.skills-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 3rem;
}

.skill-category {
  background-color: var(--bg-secondary);
  padding: 2rem;
  border-radius: 10px;
  box-shadow: var(--shadow);
}

.skill-category h3 {
  margin-bottom: 1.5rem;
  color: var(--primary-color);
}

.skills-list {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.skill-item {
  width: 100%;
}

.skill-info {
  display: flex;
  justify-content: space-between;
  margin-bottom: 0.5rem;
}

.skill-name {
  font-weight: 500;
}

.skill-level {
  color: var(--text-secondary);
}

.skill-bar {
  height: 8px;
  background-color: #e9ecef;
  border-radius: 4px;
  overflow: hidden;
}

.skill-progress {
  height: 100%;
  border-radius: 4px;
  background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
  transition: width 1s ease-in-out;
}

@media (max-width: 768px) {
  .skills-grid {
    grid-template-columns: 1fr;
  }
}
</style>