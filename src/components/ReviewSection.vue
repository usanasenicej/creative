<template>
  <section class="review-section">
    <div class="container fade-in">
      <div class="review-header">
        <h2 class="section-title">What our <span class="green-text pill">Clients Say</span></h2>
      </div>
      
      <div class="review-carousel">
        <div v-for="(review, index) in reviews" :key="index" class="review-card" :class="{ active: activeIndex === index }">
          <div class="review-content">
            <div class="quote-icon">"</div>
            <div class="review-text-container">
              <div class="trust-stars">★★★★★</div>
              <p class="review-text">{{ review.text }}</p>
            </div>
            <div class="review-footer">
              <img :src="review.image" :alt="review.name" class="reviewer-img">
              <div class="reviewer-info">
                <div class="name-row">
                  <h4 class="reviewer-name">{{ review.name }}</h4>
                  <div class="verified-badge pill">
                    <span class="check">✓</span> Verified
                  </div>
                </div>
                <p class="reviewer-role">{{ review.role }}</p>
              </div>
            </div>
          </div>
        </div>
        
        <div class="carousel-nav">
          <button @click="prev" class="nav-btn pill">←</button>
          <div class="dots">
            <div v-for="(r, i) in reviews" :key="i" class="dot" :class="{ active: activeIndex === i }" @click="activeIndex = i"></div>
          </div>
          <button @click="next" class="nav-btn pill">→</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const activeIndex = ref(0)
const reviews = [
  {
    name: 'Sarah Jenkins',
    role: 'Marketing Director, TechCorp',
    text: 'Working with Creatix has been a game-changer for our brand. Their creative vision and technical expertise are unmatched.',
    image: 'https://images.unsplash.com/photo-1544005313-94ddf0286df2?auto=format&fit=crop&q=80&w=400'
  },
  {
    name: 'Michael Chen',
    role: 'Founder, EcoDrive',
    text: 'The UI/UX design they delivered exceeded our expectations. Our user engagement has increased by 40% since the launch.',
    image: 'https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?auto=format&fit=crop&q=80&w=400'
  },
  {
    name: 'Alice Brown',
    role: 'CEO, CreativePulse',
    text: 'A truly exceptional agency. They listen, understand, and deliver high-quality results every single time.',
    image: 'https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&q=80&w=400'
  }
]

const next = () => {
  activeIndex.value = (activeIndex.value + 1) % reviews.length
}

const prev = () => {
  activeIndex.value = (activeIndex.value - 1 + reviews.length) % reviews.length
}
</script>

<style scoped>
.review-section {
  background-color: var(--bg-dark);
  padding: 120px 0;
  border-top: 1px solid rgba(255, 255, 255, 0.05);
}

.review-header {
  text-align: center;
  margin-bottom: 80px;
}

.section-title {
  font-size: 3.5rem;
  font-weight: 800;
  color: #fff;
}

.green-text {
  background: var(--accent-green);
  color: #000;
  padding: 8px 30px;
  display: inline-block;
}

.review-carousel {
  max-width: 900px;
  margin: 0 auto;
  position: relative;
}

.review-card {
  display: none;
  background: #111;
  border: 1px solid rgba(255, 255, 255, 0.1);
  padding: 60px;
  border-radius: 40px;
  position: relative;
}

.review-card.active {
  display: block;
}

.quote-icon {
  font-size: 8rem;
  color: var(--accent-green);
  font-family: serif;
  position: absolute;
  top: 10px;
  left: 40px;
  opacity: 0.1;
  line-height: 1;
}

.trust-stars {
  color: var(--accent-green);
  font-size: 1.2rem;
  margin-bottom: 15px;
  letter-spacing: 2px;
}

.review-text {
  font-size: 1.8rem;
  font-weight: 500;
  line-height: 1.4;
  color: #fff;
  margin-bottom: 40px;
  position: relative;
  z-index: 10;
}

.review-footer {
  display: flex;
  align-items: center;
  gap: 20px;
}

.reviewer-img {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  object-fit: cover;
  border: 2px solid var(--accent-green);
}

.name-row {
  display: flex;
  align-items: center;
  gap: 12px;
}

.verified-badge {
  background: rgba(255, 255, 255, 0.05);
  font-size: 0.75rem;
  padding: 4px 10px;
  color: var(--text-dim);
  border: 1px solid rgba(255, 255, 255, 0.1);
  display: flex;
  align-items: center;
  gap: 4px;
}

.verified-badge .check {
  color: var(--accent-green);
  font-weight: 900;
}

.reviewer-name {
  font-size: 1.2rem;
  font-weight: 700;
  color: #fff;
}

.reviewer-role {
  font-size: 0.9rem;
  color: var(--text-dim);
}

.carousel-nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-top: 40px;
}

.nav-btn {
  width: 50px;
  height: 50px;
  background: #222;
  color: #fff;
  font-size: 1.2rem;
}

.nav-btn:hover {
  background: var(--accent-green);
  color: #000;
}

.dots {
  display: flex;
  gap: 12px;
}

.dot {
  width: 10px;
  height: 10px;
  background: #333;
  border-radius: 50%;
  cursor: pointer;
}

.dot.active {
  background: var(--accent-green);
  width: 25px;
  border-radius: 10px;
}

@media (max-width: 768px) {
  .section-title { font-size: 2.5rem; }
  .review-text { font-size: 1.2rem; }
  .review-card { padding: 30px; }
}
</style>
