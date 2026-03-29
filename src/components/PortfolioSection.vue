<template>
  <section class="portfolio-section">
    <div class="container container-wide">
      <!-- Top Row: Title & Text -->
      <div class="portfolio-header">
        <h2 class="section-title">Turning Ideas Into <br> Masterpieces</h2>
        <div class="section-text-container">
          <p class="section-text">
            We may be a compact team, but our creativity knows no bounds. By staying agile and working hand-in-hand with our clients, we transform ideas into cutting-edge designs that make a lasting impression.
          </p>
        </div>
      </div>
      
      <!-- Bottom Row: Images Grid -->
      <div class="portfolio-grid">
        <!-- Landscape Project -->
        <div class="project-card landscape">
          <div class="green-plus-tag">+</div>
          <img src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?auto=format&fit=crop&q=80&w=1400" alt="Team Collaboration" class="project-img grayscale">
          <div class="badge-label pill">
            <span class="badge-accent"></span>
            A CREATIVE DESIGN <br> <strong>AGENCY</strong>
          </div>
        </div>
        
        <!-- Portrait Project -->
        <div class="project-card portrait">
          <div class="lightbulb-doodle">
            <svg viewBox="0 0 100 100" class="doodle-svg">
              <path d="M50,10 Q60,10 65,20 T65,40 T50,55" stroke="#FF5C5C" stroke-width="2" fill="none" />
              <path d="M50,10 Q40,10 35,20 T35,40 T50,55" stroke="#FF5C5C" stroke-width="2" fill="none" />
              <line x1="40" y1="60" x2="60" y2="60" stroke="#FF5C5C" stroke-width="2" />
              <line x1="42" y1="65" x2="58" y2="65" stroke="#FF5C5C" stroke-width="2" />
              <path d="M50,5 L50,0 M75,25 L80,20 M25,25 L20,20 M85,50 L90,50 M15,50 L10,50" stroke="#FF5C5C" stroke-width="2" />
            </svg>
          </div>
          <img src="https://images.unsplash.com/photo-1567532939604-b6c5b0ad2e01?auto=format&fit=crop&q=80&w=800" alt="Happy Creative" class="project-img grayscale">
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.portfolio-section {
  background-color: var(--bg-dark);
  padding: 120px 0;
}

.container-wide {
  max-width: 1400px;
}

.portfolio-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 80px;
}

.section-title {
  font-size: 4rem;
  font-weight: 800;
  color: #fff;
  line-height: 1.1;
  letter-spacing: -2px;
}

.section-text-container {
  max-width: 500px;
  text-align: right;
  margin-top: 20px;
}

.section-text {
  color: var(--text-dim);
  font-size: 1rem;
  line-height: 1.6;
}

.portfolio-grid {
  display: flex;
  gap: 30px;
  height: 650px;
}

.project-card {
  position: relative;
  border-radius: 40px;
  overflow: hidden;
  background: #111;
  transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
}

.project-card:hover { transform: scale(0.98); }

.landscape { flex: 1.7; height: 100%; }
.portrait { flex: 1; height: 100%; }

.project-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: filter 0.6s ease, transform 0.6s ease;
}

.grayscale { filter: grayscale(100%) brightness(0.9) contrast(1.1); }

.project-card:hover .project-img {
  filter: grayscale(0%) brightness(1);
  transform: scale(1.05);
}

.green-plus-tag {
  position: absolute;
  top: 40px;
  left: 40px;
  background: var(--accent-green);
  color: #000;
  width: 40px;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 8px; /* Slightly rounded square */
  font-size: 2rem;
  font-weight: 300;
  z-index: 10;
}

.badge-label {
  position: absolute;
  bottom: 40px;
  left: 40px;
  background: var(--accent-green);
  padding: 24px 40px 24px 30px;
  color: #000;
  display: flex;
  align-items: center;
  gap: 20px;
  z-index: 10;
  line-height: 1.2;
}

.badge-accent {
  width: 5px;
  height: 40px;
  background: #000;
  border-radius: 10px;
}

.lightbulb-doodle {
  position: absolute;
  top: 30px;
  left: 50%;
  transform: translateX(-50%);
  width: 100px;
  height: 100px;
  z-index: 10;
}

.doodle-svg { width: 100%; height: 100%; }

@media (max-width: 1024px) {
  .portfolio-grid { flex-direction: column; height: auto; }
  .landscape, .portrait { height: 400px; flex: none; }
  .portfolio-header { flex-direction: column; text-align: left; }
  .section-text-container { text-align: left; max-width: 100%; }
  .section-title { font-size: 3rem; }
}
</style>
