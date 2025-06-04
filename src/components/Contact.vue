<template>
  <section id="contact" class="contact section">
    <div class="container">
      <h2>Hubungi Saya</h2>
      <div class="contact-content">
        <div class="contact-info">
          <h3>Mari berbincang seputar perancangan proyek!</h3>
          <p>Saat ini saya tersedia untuk pekerjaan freelance atau posisi waktu penuh.
             Jangan ragu untuk menghubungi saya jika Anda ingin berkolaborasi atau sekadar menyapa!</p>
          <div class="contact-details">
            <div class="detail-item">
              <span class="icon">📧</span>
              <span>mzakijauhari@gmail.com</span>
            </div>
            <div class="detail-item">
              <span class="icon">📱</span>
              <span>+62 821-7464-1091</span>
            </div>
            <div class="detail-item">
              <span class="icon">📍</span>
              <span>Pekanbaru, Riau, Indonesia</span>
            </div>
          </div>
          <div class="social-links">
            <a href="https://github.com/zakijauhari" target="_blank" class="social-link">GitHub</a>
            <a href="https://www.instagram.com/zakijauhr/" target="_blank" class="social-link">Instagram</a>
          </div>
        </div>
        <form class="contact-form" @submit.prevent="handleSubmit">
          <div class="form-group">
            <label for="name">Nama</label>
            <input type="text" id="name" v-model="form.name" required>
          </div>
          <div class="form-group">
            <label for="email">Email</label>
            <input type="email" id="email" v-model="form.email" required>
          </div>
          <div class="form-group">
            <label for="subject">Subjek</label>
            <input type="text" id="subject" v-model="form.subject" required>
          </div>
          <div class="form-group">
            <label for="message">Pesan</label>
            <textarea id="message" v-model="form.message" rows="5" required></textarea>
          </div>
          <button type="submit" class="btn">Kirim Pesan</button>
        </form>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Contact',
  data() {
    return {
      form: {
        name: '',
        email: '',
        subject: '',
        message: ''
      }
    }
  },
  methods: {
    handleSubmit() {
      // Here you would typically send the form data to a server
      console.log('Form submitted:', this.form)
      alert('Thank you for your message! I will get back to you soon.')
      this.resetForm()
    },
    resetForm() {
      this.form = {
        name: '',
        email: '',
        subject: '',
        message: ''
      }
    }
  }
}
</script>

<style scoped>
.contact-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 3rem;
  align-items: start;
}

.contact-info h3 {
  font-size: 1.5rem;
  margin-bottom: 1.5rem;
  color: var(--primary-color);
}

.contact-info p {
  margin-bottom: 2rem;
}

.contact-details {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  margin-bottom: 2rem;
}

.detail-item {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.detail-item .icon {
  font-size: 1.2rem;
}

.social-links {
  display: flex;
  gap: 1.5rem;
}

.social-link {
  font-weight: 500;
  position: relative;
}

.social-link::after {
  content: '';
  position: absolute;
  bottom: -3px;
  left: 0;
  width: 0;
  height: 2px;
  background-color: var(--primary-color);
  transition: var(--transition);
}

.social-link:hover::after {
  width: 100%;
}

.contact-form {
  background-color: var(--bg-secondary);
  padding: 2rem;
  border-radius: 10px;
  box-shadow: var(--shadow);
}

.form-group {
  margin-bottom: 1.5rem;
}

.form-group label {
  display: block;
  margin-bottom: 0.5rem;
  font-weight: 500;
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 0.8rem;
  border: 1px solid #ddd;
  border-radius: 5px;
  font-family: inherit;
  background-color: var(--bg-primary);
  color: var(--text-primary);
  transition: var(--transition);
}

.form-group input:focus,
.form-group textarea:focus {
  outline: none;
  border-color: var(--primary-color);
  box-shadow: 0 0 0 2px rgba(58, 134, 255, 0.2);
}

button[type="submit"] {
  width: 100%;
}

@media (max-width: 768px) {
  .contact-content {
    grid-template-columns: 1fr;
  }
}
</style>