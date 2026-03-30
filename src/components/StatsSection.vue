<template>
  <section class="stats-section">
    <div class="container">
      <div class="stats-pill pill">
        <div v-for="(stat, index) in stats" :key="index" class="stat-item">
          <div class="stat-number">{{ stat.number }}</div>
          <div class="stat-label">{{ stat.label }}</div>
          <div v-if="index !== stats.length - 1" class="stat-divider"></div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const stats = [
  { number: '2000+', label: 'Company' },
  { number: '10+', label: 'Years Exp.' },
  { number: '800+', label: 'Hours of Digital' },
  { number: '150M+', label: 'In Tracked Revenue' }
]
</script>

<style scoped>
.stats-section {
  background-color: var(--bg-dark);
  padding: 40px 0;
  margin-top: -60px; /* Overlap with hero bottom */
  z-index: 100;
  position: relative;
}

.stats-pill {
  background: #111;
  border: 1px solid rgba(255, 255, 255, 0.1);
  display: flex;
  justify-content: space-around;
  padding: 40px 60px;
  box-shadow: 0 40px 80px rgba(0, 0, 0, 0.6), 0 0 20px rgba(182, 255, 0, 0.05);
  border-radius: 40px;
  transition: all 0.4s ease;
}

.stats-pill:hover {
  border-color: rgba(182, 255, 0, 0.2);
  box-shadow: 0 50px 100px rgba(0, 0, 0, 0.8), 0 0 30px rgba(182, 255, 0, 0.1);
}

.stat-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
  position: relative;
  flex: 1;
  transition: transform 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}

.stat-item:hover {
  transform: translateY(-5px);
}

.stat-divider {
  position: absolute;
  right: 0;
  top: 10%;
  height: 80%;
  width: 1px;
  background: linear-gradient(to bottom, transparent, rgba(255, 255, 255, 0.1), transparent);
}

.stat-number {
  font-size: 2.2rem;
  font-weight: 800;
  color: #fff;
  transition: color 0.3s ease;
}

.stat-item:hover .stat-number {
  color: var(--accent-green);
}

.stat-label {
  font-size: 0.85rem;
  color: var(--text-dim);
  text-transform: uppercase;
  letter-spacing: 1px;
}

@media (max-width: 768px) {
  .stats-pill {
    flex-direction: column;
    padding: 30px;
    gap: 30px;
    border-radius: 30px;
  }
  
  .stat-divider { display: none; }
  .stat-number { font-size: 1.8rem; }
}
</style>
