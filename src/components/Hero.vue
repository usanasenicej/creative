<template>
  <section class="hero-section">
    <!-- Hero White Background -->
    <div class="hero-white-container">
      <div class="container hero-inner">
        
        <!-- Top Title & Sparkles -->
        <div class="hero-header">
          <div class="sparkle left-sparkle"></div>
          <h1 class="hero-title">Empowering Brands <br> Through <span>Creative Solutions</span></h1>
          <div class="sparkle right-sparkle"></div>
        </div>

        <!-- Main Content Area with Woman and Badges -->
        <div class="hero-content">
          <!-- Floating Badges and Icons -->
          <div class="badge-area left-badge">
            <button class="renovate-btn pill">Renovate Your Brand</button>
            <p class="description-text">From web development to branding, we deliver innovative strategies that elevate your brand and drive growth. Let's create something exceptional together.</p>
            <div class="squiggle-arrow">
              <svg viewBox="0 0 100 100" class="squiggle-svg">
                <path d="M10,80 Q30,20 60,60 T90,40" stroke="#000" stroke-width="2" fill="none" />
                <path d="M85,35 L90,40 L85,45" stroke="#000" stroke-width="2" fill="none" />
              </svg>
            </div>
          </div>

          <div class="woman-image-wrapper">
            <div class="gray-bg-circle"></div>
            <img src="https://images.unsplash.com/photo-1573497019940-1c28c88b4f3e?auto=format&fit=crop&q=80&w=1000" alt="Creative Professional Cheering" class="hero-woman-img">
            
            <!-- Bottom CTA Pill -->
            <div class="cta-floating-pill pill glass">
              <button class="btn btn-green pill">Start Your Project</button>
              <button class="btn btn-transparent">Let's Collaborate</button>
            </div>
          </div>

          <div class="badge-area right-badge">
            <div class="stars-row">
              <div v-for="i in 5" :key="i" class="star">★</div>
            </div>
            <div class="experience-text">
              <strong>10 Years</strong>
              <span>Experience</span>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<style scoped>
.hero-section {
  background-color: var(--bg-dark);
  padding: 100px 20px 0;
  min-height: auto;
}

.hero-white-container {
  background: #fff;
  border-radius: 60px 60px 200px 200px;
  width: 100%;
  max-width: 1400px;
  min-height: 700px;
  margin: 0 auto;
  position: relative;
  overflow: hidden;
  padding: 60px 40px;
}

.hero-inner {
  display: flex;
  flex-direction: column;
  align-items: center;
}

/* Header & Sparkles */
.hero-header {
  position: relative;
  text-align: center;
  margin-bottom: 40px;
}

.hero-title {
  font-size: 4rem;
  font-weight: 800;
  color: #000;
  letter-spacing: -2px;
  line-height: 1.1;
  position: relative;
  z-index: 10;
}

.sparkle {
  position: absolute;
  width: 60px;
  height: 60px;
  background: var(--accent-green);
  mask: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24'%3E%3Cpath d='M12 0l3.09 6.26L22 7.27l-5 4.87L18.18 19 12 15.77 5.82 19 7 12.14 2 7.27l6.91-1.01L12 0z'/%3E%3C/svg%3E") no-repeat center;
  -webkit-mask: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24'%3E%3Cpath d='M12 0l3.09 6.26L22 7.27l-5 4.87L18.18 19 12 15.77 5.82 19 7 12.14 2 7.27l6.91-1.01L12 0z'/%3E%3C/svg%3E") no-repeat center;
}

.left-sparkle { top: -20px; left: -80px; transform: rotate(-15deg); }
.right-sparkle { bottom: -10px; right: -80px; transform: rotate(15deg); }

/* Content Area */
.hero-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  max-width: 1100px;
  margin-top: 20px;
  position: relative;
}

.badge-area { display: flex; flex-direction: column; gap: 20px; width: 250px; }

.renovate-btn {
  background: transparent;
  border: 1px solid #000;
  padding: 10px 24px;
  font-size: 0.9rem;
  font-weight: 600;
  color: #000;
  width: fit-content;
}

.description-text {
  font-size: 0.9rem;
  color: #666;
  line-height: 1.5;
  text-align: left;
}

.squiggle-arrow {
  width: 80px;
  height: 80px;
  margin-left: 20px;
  opacity: 0.8;
}

.woman-image-wrapper {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: -50px;
}

.gray-bg-circle {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 450px;
  height: 450px;
  background: radial-gradient(circle, #e0e0e0 0%, transparent 70%);
  border-radius: 50%;
  z-index: 1;
}

.hero-woman-img {
  width: 100%;
  max-width: 500px;
  z-index: 5;
  filter: contrast(1.05);
}

.cta-floating-pill {
  background: rgba(0, 0, 0, 0.85);
  border: 1px solid rgba(255, 255, 255, 0.1);
  padding: 8px;
  display: flex;
  align-items: center;
  gap: 10px;
  position: absolute;
  bottom: 40px;
  z-index: 20;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);
}

.btn-green {
  background: var(--accent-green);
  color: #000;
  padding: 14px 28px;
  font-weight: 700;
  font-size: 0.9rem;
}

.btn-transparent {
  background: transparent;
  color: #fff;
  padding: 14px 28px;
  font-weight: 600;
}

/* Right Badge area */
.right-badge { align-items: flex-end; text-align: right; }

.stars-row { display: flex; gap: 4px; color: var(--accent-green); font-size: 1.2rem; }

.experience-text { display: flex; flex-direction: column; align-items: flex-end; gap: 4px; }
.experience-text strong { font-size: 2.2rem; font-weight: 800; color: #000; }
.experience-text span { font-size: 0.9rem; color: #666; text-transform: uppercase; letter-spacing: 1px;}

@media (max-width: 1200px) {
  .hero-title { font-size: 3.5rem; }
  .left-sparkle, .right-sparkle { display: none; }
  .badge-area { display: none; }
}
</style>
