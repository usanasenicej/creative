<template>
  <section class="portfolio-section">
    <div class="container">
      <div class="portfolio-header">
        <h2 class="section-title">Turning Ideas Into <br> <span class="text-white">Masterpieces</span></h2>
        <p class="section-text">
          We may be a compact team, but our creativity knows no bounds. By staying agile and working hand-in-hand with our clients, we transform ideas into cutting-edge designs that make a lasting impression.
        </p>
      </div>
      
      <div class="portfolio-grid">
        <div class="portfolio-item-large">
          <img src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?auto=format&fit=crop&q=80&w=1400" alt="Team Work" class="portfolio-img grayscale">
          <div class="item-overlay floating-green pill">
            <span class="overlay-text">A CREATIVE DESIGN <br> <strong>AGENCY</strong></span>
          </div>
          <div class="star-accent plus">+</div>
        </div>
        
        <div class="portfolio-item-small">
          <img src="https://images.unsplash.com/photo-1573164713988-8665fc963095?auto=format&fit=crop&q=80&w=800" alt="Creative Workspace" class="portfolio-img grayscale">
          <div class="lightbulb-icon">💡</div>
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

.portfolio-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  margin-bottom: 60px;
}

.section-title {
  font-size: 3.5rem;
  font-weight: 800;
  color: var(--text-dim);
  line-height: 1;
}

.section-text {
  max-width: 450px;
  color: var(--text-dim);
  font-size: 1rem;
  line-height: 1.6;
}

.portfolio-grid {
  display: grid;
  grid-template-columns: 1.6fr 1fr;
  gap: 30px;
  height: 600px;
}

.portfolio-item-large, .portfolio-item-small {
  position: relative;
  border-radius: 40px;
  overflow: hidden;
  height: 100%;
}

.portfolio-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.6s ease;
}

.grayscale {
  filter: grayscale(100%);
}

.portfolio-item-large:hover .portfolio-img, 
.portfolio-item-small:hover .portfolio-img {
  transform: scale(1.05);
  filter: grayscale(0%);
}

.floating-green {
  position: absolute;
  bottom: 40px;
  left: 40px;
  background: var(--accent-green);
  padding: 20px 30px;
  color: #000;
  display: flex;
  align-items: center;
  transition: transform 0.3s ease;
}

.overlay-text {
  font-size: 0.9rem;
  line-height: 1.2;
}

.star-accent {
  position: absolute;
  top: 40px;
  left: 40px;
  font-size: 3rem;
  color: var(--accent-green);
  font-weight: 300;
}

.lightbulb-icon {
  position: absolute;
  top: 40px;
  right: 40px;
  font-size: 2.5rem;
  filter: drop-shadow(0 0 10px rgba(255, 255, 0, 0.5));
}

@media (max-width: 1024px) {
  .portfolio-grid {
    grid-template-columns: 1fr;
    height: auto;
  }
  
  .portfolio-item-large, .portfolio-item-small {
    height: 400px;
  }
  
  .portfolio-header {
    flex-direction: column;
    align-items: flex-start;
    gap: 30px;
  }
  
  .section-title { font-size: 2.5rem; }
}
</style>
