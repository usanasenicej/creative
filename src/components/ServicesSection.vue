<template>
  <section class="services-section">
    <div class="container services-grid">
      <div class="services-info">
        <div class="service-badge pill">
          <span>Our Services</span>
        </div>
        
        <h2 class="services-title">We offer a range of creative and digital services designed to help your brand stand out.</h2>
        
        <div class="services-list">
          <div v-for="(service, index) in services" :key="index" class="service-item pill">
            <div class="service-index">{{ service.id }}</div>
            <div class="service-label">{{ service.title }}</div>
            <div class="service-arrow">→</div>
          </div>
        </div>
      </div>
      
      <div class="services-visual">
        <div class="visual-main-card">
          <img src="https://images.unsplash.com/photo-1581091226825-a6a2a5aee158?auto=format&fit=crop&q=80&w=1000" alt="Service Deep Dive" class="visual-img">
          
          <div class="visual-side-text">
            <span>See how<br>we work</span>
            <div class="side-arrow pill">
              <span>→</span>
            </div>
          </div>
        </div>
        
        <div class="expert-card pill">
          <p class="expert-text">Looking for design experts who can bring your vision to life?</p>
          <button class="expert-btn pill">Meet our expert <span class="arrow-up-right">↗</span></button>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const services = [
  { id: '01', title: 'UI/UX Design' },
  { id: '02', title: 'Web Development' },
  { id: '03', title: '3D Designs' },
  { id: '04', title: 'Motion Graphics' }
]
</script>

<style scoped>
.services-section {
  background-color: var(--bg-dark);
  padding: 120px 0;
}

.services-grid {
  display: grid;
  grid-template-columns: 1.2fr 1.5fr;
  gap: 80px;
}

.services-info {
  display: flex;
  flex-direction: column;
  gap: 30px;
}

.service-badge {
  display: inline-flex;
  background: var(--accent-green);
  color: #000;
  padding: 8px 24px;
  font-weight: 800;
  font-size: 1.1rem;
  width: fit-content;
  box-shadow: 0 0 30px rgba(163, 255, 46, 0.4);
}

.services-title {
  font-size: 1.8rem;
  font-weight: 500;
  color: var(--text-main);
  line-height: 1.4;
  margin-bottom: 20px;
}

.services-list {
  display: flex;
  flex-direction: column;
  gap: 16px;
}

.service-item {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 24px 40px;
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.1);
  transition: var(--transition);
  cursor: pointer;
}

.service-item:hover {
  background: rgba(255, 255, 255, 0.1);
  transform: translateX(10px);
  border-color: var(--accent-green);
}

.service-index {
  font-size: 1.4rem;
  font-weight: 800;
  color: var(--accent-green);
}

.service-label {
  font-size: 1.2rem;
  font-weight: 600;
  flex-grow: 1;
  margin-left: 30px;
}

.service-arrow {
  font-size: 1.5rem;
  transition: transform 0.3s ease;
}

.service-item:hover .service-arrow {
  transform: translateX(5px);
  color: var(--accent-green);
}

.services-visual {
  position: relative;
}

.visual-main-card {
  height: 600px;
  border-radius: 40px;
  overflow: hidden;
  position: relative;
}

.visual-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  filter: contrast(1.1) brightness(0.9);
}

.visual-side-text {
  position: absolute;
  top: 40px;
  right: 40px;
  text-align: right;
  color: #fff;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  gap: 15px;
}

.visual-side-text span {
  font-size: 1.2rem;
  font-weight: 700;
  line-height: 1.2;
}

.side-arrow {
  width: 60px;
  height: 60px;
  background: #222;
  display: flex;
  align-items: center;
  justify-content: center;
  border: 1px solid rgba(255, 255, 255, 0.2);
  font-size: 1.5rem;
}

.expert-card {
  position: absolute;
  bottom: 0;
  right: -40px;
  background: var(--accent-green);
  width: 300px;
  padding: 40px;
  color: #000;
  display: flex;
  flex-direction: column;
  gap: 20px;
  transform: translateY(20%);
  box-shadow: 0 30px 60px rgba(0, 0, 0, 0.4);
}

.expert-text {
  font-weight: 600;
  font-size: 1.1rem;
  line-height: 1.3;
}

.expert-btn {
  background: #fff;
  color: #000;
  padding: 16px 24px;
  font-weight: 700;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
}

.expert-btn:hover {
  background: #000;
  color: #fff;
}

@media (max-width: 1024px) {
  .services-grid {
    grid-template-columns: 1fr;
    gap: 60px;
  }
  
  .expert-card {
    position: relative;
    right: 0;
    width: 100%;
    transform: none;
    margin-top: 40px;
  }
  
  .visual-main-card {
    height: 400px;
  }
}
</style>
