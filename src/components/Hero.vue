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
            <p class="description-text">From web-development to branding, we deliver innovative strategies that elevate your brand and drive growth. let's create something exceptional together.</p>
            <button class="renovate-btn pill">Renovate Your Brand</button>
            <div class="squiggle-arrow">
              <svg viewBox="0 0 100 100" class="squiggle-svg">
                <path d="M10,80 Q30,20 60,60 T90,40" stroke="#111" stroke-width="2" fill="none" />
                <path d="M85,35 L90,40 L85,45" stroke="#111" stroke-width="2" fill="none" />
              </svg>
            </div>
          </div>

          <div class="woman-image-wrapper">
            <div class="subtle-grey-circle"></div>
            <img src="https://images.unsplash.com/photo-1573497019940-1c28c88b4f3e?auto=format&fit=crop&q=80&w=1000" alt="Creative Professional Cheering" class="hero-woman-img">
            
            <!-- Bottom CTA Pill - EXACT UI Match -->
            <div class="cta-floating-pill pill-dark">
              <button class="btn-green pill">Start Your Project</button>
              <button class="btn-text">Let's Collaborate</button>
            </div>
          </div>

          <div class="badge-area right-badge">
            <div class="stars-row">
              <div v-for="i in 5" :key="i" class="star">★</div>
            </div>
            <div class="experience-text">
              <strong class="text-black">10 Years</strong>
              <span class="text-gray">Experience</span>
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
  padding: 80px 20px 0; /* Slightly more compact as per user request */
  min-height: auto;
}

.hero-white-container {
  background: #fff;
  border-radius: 60px 60px 180px 180px; /* More moderate rounded bottom */
  width: 100%;
  max-width: 1300px;
  min-height: 650px;
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
  margin-bottom: 20px;
}

.hero-title {
  font-size: 3.5rem; /* Reduced as requested */
  font-weight: 800;
  color: #000;
  letter-spacing: -2px;
  line-height: 1.1;
  position: relative;
  z-index: 10;
}

.sparkle {
  position: absolute;
  width: 50px;
  height: 50px;
  background: var(--accent-green);
  mask: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24'%3E%3Cpath d='M12 0l3.09 6.26L22 7.27l-5 4.87L18.18 19 12 15.77 5.82 19 7 12.14 2 7.27l6.91-1.01L12 0z'/%3E%3C/svg%3E") no-repeat center;
  -webkit-mask: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24'%3E%3Cpath d='M12 0l3.09 6.26L22 7.27l-5 4.87L18.18 19 12 15.77 5.82 19 7 12.14 2 7.27l6.91-1.01L12 0z'/%3E%3C/svg%3E") no-repeat center;
}

.left-sparkle { top: -20px; left: -60px; transform: scaleY(0.8); }
.right-sparkle { bottom: 0; right: -60px; transform: scaleX(0.8) rotate(15deg); }

/* Content Area */
.hero-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  max-width: 1100px;
  margin-top: 10px;
  position: relative;
}

.badge-area { display: flex; flex-direction: column; gap: 20px; width: 200px; }

.renovate-btn {
  background: transparent;
  border: 1.5px solid #000;
  padding: 10px 24px;
  font-size: 0.85rem;
  font-weight: 600;
  color: #000;
  width: fit-content;
  opacity: 0.8;
}

.description-text {
  font-size: 0.85rem;
  color: #777;
  line-height: 1.4;
  text-align: left;
}

.squiggle-arrow {
  width: 100px;
  height: 100px;
  position: absolute;
  left: 140px;
  top: 120px;
  opacity: 0.6;
}

.woman-image-wrapper {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: -30px;
}

.subtle-grey-circle {
  position: absolute;
  top: 45%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 420px;
  height: 420px;
  background: #F4F4F4;
  border-radius: 50%;
  z-index: 1;
}

.hero-woman-img {
  width: 100%;
  max-width: 480px;
  z-index: 5;
  position: relative;
}

/* Bottom CTA Pill-Dark EXACT UI */
.cta-floating-pill {
  background: #111;
  border-radius: 99px;
  padding: 6px;
  display: flex;
  align-items: center;
  gap: 15px;
  position: absolute;
  bottom: 30px;
  left: 50%;
  transform: translateX(-50%);
  z-index: 20;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
}

.btn-green {
  background: var(--accent-green);
  color: #000;
  padding: 12px 28px;
  font-weight: 700;
  font-size: 0.9rem;
  cursor: pointer;
}

.btn-text {
  background: transparent;
  color: #fff;
  border: none;
  font-weight: 500;
  font-size: 0.9rem;
  padding: 0 20px 0 5px;
  cursor: pointer;
  opacity: 0.9;
}

.btn-text:hover { opacity: 1; color: var(--accent-green); }

/* Right Badge area */
.right-badge { align-items: flex-end; text-align: right; margin-top: 40px; }

.stars-row { display: flex; gap: 4px; color: var(--accent-green); font-size: 1.2rem; margin-bottom: 8px; }

.experience-text { display: flex; flex-direction: column; align-items: flex-end; gap: 0; }
.experience-text strong { font-size: 2.2rem; font-weight: 800; color: #000; line-height: 1; }
.experience-text span { font-size: 0.85rem; color: #888; text-transform: uppercase; letter-spacing: 0.5px; }

@media (max-width: 1200px) {
  .hero-title { font-size: 3rem; }
  .badge-area, .squiggle-arrow { display: none; }
  .hero-white-container { min-height: 550px; }
}
</style>
