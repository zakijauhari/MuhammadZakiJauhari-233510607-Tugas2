<template>
  <header class="header">
    <div class="container">
      <nav class="nav">
        <div class="logo">
          <span>ZJ</span>
        </div>
        <ul class="nav-links">
          <li><a href="#about">Tentang Saya</a></li>
          <li><a href="#skills">Keterampilan</a></li>
          <li><a href="#projects">Proyek Saya</a></li>
          <li><a href="#contact">Kontak</a></li>
          <li>
            <button @click="toggleDarkMode" class="theme-toggle">
              <span v-if="darkMode">☀️</span>
              <span v-else>🌙</span>
            </button>
          </li>
        </ul>
        <button class="hamburger" @click="toggleMenu">
          <span></span>
          <span></span>
          <span></span>
        </button>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      darkMode: false,
      menuOpen: false
    }
  },
  methods: {
    toggleDarkMode() {
      this.darkMode = !this.darkMode
      document.documentElement.classList.toggle('dark-mode', this.darkMode)
    },
    toggleMenu() {
      this.menuOpen = !this.menuOpen
      document.querySelector('.nav-links').classList.toggle('active', this.menuOpen)
    }
  }
}
</script>

<style scoped>
.header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1000;
  background-color: var(--bg-secondary);
  box-shadow: var(--shadow);
  padding: 1rem 0;
}

.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--primary-color);
}

.logo span {
  background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
}

.nav-links {
  display: flex;
  list-style: none;
  gap: 2rem;
}

.nav-links li a {
  font-weight: 500;
  position: relative;
}

.nav-links li a::after {
  content: '';
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 0;
  height: 2px;
  background-color: var(--primary-color);
  transition: var(--transition);
}

.nav-links li a:hover::after {
  width: 100%;
}

.theme-toggle {
  background: none;
  border: none;
  font-size: 1.2rem;
  cursor: pointer;
  transition: var(--transition);
}

.theme-toggle:hover {
  transform: scale(1.1);
}

.hamburger {
  display: none;
  background: none;
  border: none;
  cursor: pointer;
  padding: 0.5rem;
}

.hamburger span {
  display: block;
  width: 25px;
  height: 3px;
  background-color: var(--text-primary);
  margin: 5px 0;
  transition: var(--transition);
}

@media (max-width: 768px) {
  .nav-links {
    position: fixed;
    top: 70px;
    left: -100%;
    width: 100%;
    height: calc(100vh - 70px);
    background-color: var(--bg-secondary);
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 2rem;
    transition: var(--transition);
  }
  
  .nav-links.active {
    left: 0;
  }
  
  .hamburger {
    display: block;
    z-index: 1001;
  }
  
  .hamburger.active span:nth-child(1) {
    transform: rotate(45deg) translate(5px, 5px);
  }
  
  .hamburger.active span:nth-child(2) {
    opacity: 0;
  }
  
  .hamburger.active span:nth-child(3) {
    transform: rotate(-45deg) translate(7px, -6px);
  }
}
</style>