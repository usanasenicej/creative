<template>
  <footer class="footer">
    <!-- Contact CTA Section -->
    <div class="footer-cta container">
      <div class="cta-inner pill glass">
        <div class="cta-text">
          <h2 class="cta-title">Get in Touch Today!</h2>
          <p class="cta-subtitle">Let's transform your vision into an exceptional digital experience. Whether you're looking to revitalize a brand or start a stunning website.</p>
          <div class="email-input-wrapper pill">
            <input type="email" placeholder="Enter your email" class="email-input">
            <button class="subscribe-btn pill">Subscribe <span class="arrow">→</span></button>
          </div>
        </div>
        <div class="cta-image-container">
          <img src="https://images.unsplash.com/photo-1544005313-94ddf0286df2?auto=format&fit=crop&q=80&w=800" alt="Contact Us" class="cta-img">
        </div>
      </div>
    </div>

    <!-- Main Footer -->
    <div class="main-footer container">
      <div class="footer-grid">
        <div class="footer-brand">
          <div class="logo">
            <div class="logo-icon"></div>
            <span class="logo-text">Creatix</span>
          </div>
          <p class="brand-desc">Empowering brands through creative solutions. We are a team of dedicated designers and developers focused on building your vision.</p>
          <div class="social-links">
            <a v-for="s in socials" :key="s" href="#" class="social-link pill">{{ s }}</a>
          </div>
        </div>

        <div class="footer-nav">
          <div class="nav-column">
            <h4>Company</h4>
            <a href="#">About Us</a>
            <a href="#">Our Team</a>
            <a href="#">Services</a>
            <a href="#">Contact</a>
          </div>
          <div class="nav-column">
            <h4>Support</h4>
            <a href="#">Help Center</a>
            <a href="#">Terms of Service</a>
            <a href="#">Privacy Policy</a>
            <a href="#">FAQ</a>
          </div>
          <div class="nav-column">
            <h4>Resources</h4>
            <a href="#">Blog</a>
            <a href="#">Cases</a>
            <a href="#">Designs</a>
            <a href="#">Tools</a>
          </div>
        </div>
      </div>

      <div class="footer-bottom">
        <p>© 2026 Creatix Agency. All rights reserved.</p>
        <div class="bottom-links">
          <span>Made with ❤️ for Creative Brands</span>
        </div>
      </div>
    </div>
    
    <!-- Large bottom green area for logo -->
    <div class="dramatic-bottom container">
      <div class="huge-logo-area pill">
        <div v-for="i in 10" :key="i" class="pixel-dot"></div>
      </div>
    </div>
  </footer>
</template>

<script setup>
const socials = ['𝕏', 'Ig', 'Li', 'Be']
</script>

<style scoped>
.footer {
  background-color: var(--bg-dark);
  padding: 120px 0 60px;
  position: relative;
}

.footer-cta {
  margin-bottom: 120px;
}

.cta-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 80px;
  position: relative;
  overflow: hidden;
  border-color: rgba(163, 255, 46, 0.2);
  background: rgba(163, 255, 46, 0.05);
}

.cta-text {
  flex: 1;
  max-width: 600px;
  z-index: 10;
}

.cta-title {
  font-size: 3.5rem;
  font-weight: 800;
  color: #fff;
  margin-bottom: 20px;
  letter-spacing: -2px;
}

.cta-subtitle {
  font-size: 1.1rem;
  color: var(--text-dim);
  margin-bottom: 40px;
  line-height: 1.6;
}

.email-input-wrapper {
  background: #222;
  padding: 10px;
  display: flex;
  gap: 10px;
  max-width: 500px;
  border: 1px solid rgba(255, 255, 255, 0.1);
}

.email-input {
  background: transparent;
  border: none;
  padding: 15px 30px;
  color: #fff;
  flex: 1;
  font-family: inherit;
  font-size: 1rem;
}

.email-input:focus { outline: none; }

.subscribe-btn {
  background: var(--accent-green);
  color: #000;
  padding: 15px 40px;
  font-weight: 700;
  font-size: 1rem;
}

.subscribe-btn:hover { background: #92e529; transform: translateY(-2px); }

.cta-image-container {
  width: 400px;
  height: 400px;
  position: relative;
}

.cta-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 50%;
  border: 8px solid rgba(163, 255, 46, 0.3);
  box-shadow: 0 0 60px rgba(163, 255, 46, 0.2);
}

.main-footer {
  padding: 80px 0;
  border-top: 1px solid rgba(255, 255, 255, 0.05);
}

.footer-grid {
  display: grid;
  grid-template-columns: 1fr 1.5fr;
  gap: 100px;
  margin-bottom: 80px;
}

.footer-brand {
  display: flex;
  flex-direction: column;
  gap: 30px;
}

.logo {
  display: flex;
  align-items: center;
  gap: 12px;
}

.logo-icon {
  width: 32px;
  height: 32px;
  background: var(--accent-green);
  clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
}

.logo-text { font-size: 1.8rem; font-weight: 800; color: #fff; }

.brand-desc {
  color: var(--text-dim);
  font-size: 1rem;
  line-height: 1.6;
}

.social-links {
  display: flex;
  gap: 15px;
}

.social-link {
  width: 45px;
  height: 45px;
  background: #111;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #fff;
  border: 1px solid rgba(255, 255, 255, 0.1);
  font-size: 1.1rem;
}

.social-link:hover {
  background: var(--accent-green);
  color: #000;
  transform: translateY(-5px);
}

.footer-nav {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 40px;
}

.nav-column {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.nav-column h4 {
  font-size: 1.1rem;
  font-weight: 700;
  color: #fff;
  margin-bottom: 10px;
}

.nav-column a {
  color: var(--text-dim);
  font-size: 1rem;
}

.nav-column a:hover { color: var(--accent-green); }

.footer-bottom {
  display: flex;
  justify-content: space-between;
  padding-top: 40px;
  border-top: 1px solid rgba(255, 255, 255, 0.05);
  color: var(--text-dim);
  font-size: 0.9rem;
}

.dramatic-bottom {
  margin-top: 60px;
}

.huge-logo-area {
  background: var(--accent-green);
  height: 120px; /* Big green bottom pill */
  display: flex;
  justify-content: space-around;
  align-items: center;
  position: relative;
  overflow: hidden;
}

.pixel-dot {
  width: 10px;
  height: 10px;
  background: #000;
  opacity: 0.1;
  border-radius: 50%;
}

@media (max-width: 1024px) {
  .footer-grid { grid-template-columns: 1fr; gap: 60px; }
  .cta-inner { flex-direction: column; padding: 40px; text-align: center; }
  .cta-image-container { display: none; }
  .cta-title { font-size: 2.5rem; }
  .footer-nav { grid-template-columns: repeat(2, 2fr); }
}
</style>
