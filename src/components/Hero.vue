<template>
  <section class="hero-section">
    <div class="hero-white-card">
      <div class="hero-content">
        <!-- Floating Elements -->
        <div class="floating-badge badge-left pill fade-in">
          <div class="icon-star"></div>
          <span class="badge-text text-black">10 Years<br><small>Experience</small></span>
        </div>
        
        <div class="floating-badge badge-right pill fade-in" style="animation-delay: 0.2s;">
          <span class="badge-text text-black">Renovate Your Brand</span>
        </div>

        <div class="hero-text-content">
          <div class="top-badge">
            <div class="green-dot"></div>
            <span>Creatix Agency</span>
          </div>
          
          <h1 class="hero-title">
            Empowering Brands<br>Through <span class="text-gradient">Creative Solutions</span>
          </h1>
          
          <p class="hero-subtitle">
            From web development to branding, we deliver innovative strategies that elevate your brand and drive growth. Let's create something exceptional together.
          </p>
          
          <div class="hero-actions">
            <button class="btn btn-green pill">Start Your Project</button>
            <button class="btn btn-outline pill">Let's Collaborate</button>
          </div>
        </div>
        
        <div class="hero-image-container">
          <!-- Using high quality Unsplash image as requested -->
          <img src="https://images.unsplash.com/photo-1580489944761-15a19d654956?auto=format&fit=crop&q=80&w=1200" alt="Creative Professional" class="hero-img">
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero-section {
  background-color: var(--bg-dark);
  padding: 120px 20px 0;
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

.hero-white-card {
  background: var(--hero-light);
  border-radius: 60px 60px 400px 400px; /* Dramatic rounded bottom */
  width: 100%;
  max-width: 1400px;
  min-height: 80vh;
  position: relative;
  display: flex;
  justify-content: center;
  overflow: hidden;
  padding: 80px 40px;
}

.hero-content {
  max-width: 1200px;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  position: relative;
}

.hero-text-content {
  z-index: 10;
  color: #000;
  max-width: 800px;
}

.top-badge {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: rgba(0, 0, 0, 0.05);
  padding: 6px 16px;
  border-radius: 99px;
  font-size: 0.9rem;
  font-weight: 600;
  margin-bottom: 24px;
}

.green-dot {
  width: 8px;
  height: 8px;
  background: var(--accent-green);
  border-radius: 50%;
  box-shadow: 0 0 10px var(--accent-green);
}

.hero-title {
  font-size: 4.5rem;
  font-weight: 800;
  letter-spacing: -2px;
  margin-bottom: 24px;
}

.text-gradient {
  background: linear-gradient(to right, #000, #444);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.hero-subtitle {
  font-size: 1.1rem;
  line-height: 1.6;
  color: #555;
  max-width: 600px;
  margin: 0 auto 40px;
}

.hero-actions {
  display: flex;
  gap: 16px;
  justify-content: center;
}

.btn {
  padding: 18px 36px;
  font-weight: 700;
  font-size: 1rem;
}

.btn-green {
  background: var(--accent-green);
  color: #000;
}

.btn-green:hover {
  background: #92e529;
  transform: translateY(-2px);
  box-shadow: 0 10px 20px rgba(163, 255, 46, 0.3);
}

.btn-outline {
  border: 2px solid #000;
  color: #000;
  background: transparent;
}

.btn-outline:hover {
  background: #000;
  color: #fff;
  transform: translateY(-2px);
}

.hero-image-container {
  margin-top: 40px;
  position: relative;
  width: 100%;
  max-width: 600px;
  display: flex;
  justify-content: center;
}

.hero-img {
  width: 100%;
  height: auto;
  object-fit: contain;
  filter: drop-shadow(0 20px 40px rgba(0, 0, 0, 0.2));
  /* Floating animation */
  animation: float 6s ease-in-out infinite;
}

.floating-badge {
  position: absolute;
  padding: 16px 24px;
  background: #fff;
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
  display: flex;
  align-items: center;
  gap: 12px;
  z-index: 20;
}

.badge-left {
  top: 300px;
  left: 100px;
}

.badge-right {
  top: 400px;
  right: 150px;
}

.badge-text { font-weight: 700; font-size: 0.9rem; text-align: left; line-height: 1.2; color: #000;}

.icon-star {
  color: #FFD700;
  font-size: 1.5rem;
  /* Visual of 5 stars */
  width: 20px;
  height: 20px;
  background-color: var(--accent-green);
  mask: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24'%3E%3Cpath d='M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z'/%3E%3C/svg%3E") no-repeat center;
  -webkit-mask: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24'%3E%3Cpath d='M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z'/%3E%3C/svg%3E") no-repeat center;
}

@keyframes float {
  0% { transform: translateY(0px); }
  50% { transform: translateY(-20px); }
  100% { transform: translateY(0px); }
}

@media (max-width: 1024px) {
  .hero-title { font-size: 3rem; }
  .badge-left, .badge-right { display: none; }
}
</style>
