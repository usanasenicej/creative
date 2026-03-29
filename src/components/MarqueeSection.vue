<template>
  <section class="marquee-section">
    <div class="marquee-container">
      <div v-for="i in 2" :key="i" class="marquee-track">
        <div v-for="(item, index) in items" :key="index" class="marquee-item">
          <span>{{ item }}</span>
          <div class="marquee-plus">+</div>
        </div>
      </div>
    </div>
    <div class="divider-line container">
      <div class="star-center">✦</div>
    </div>
  </section>
</template>

<script setup>
const items = ['Innovate', 'Inspire', 'Create']
</script>

<style scoped>
.marquee-section {
  background-color: var(--bg-dark);
  padding: 60px 0;
  overflow: hidden;
  position: relative;
}

.marquee-container {
  display: flex;
  overflow: hidden;
  gap: 60px;
  user-select: none;
}

.marquee-track {
  display: flex;
  flex-shrink: 0;
  gap: 60px;
  min-width: 100%;
  animation: scroll 20s linear infinite;
}

.marquee-item {
  display: flex;
  align-items: center;
  gap: 60px;
  font-size: 5rem;
  font-weight: 800;
  text-transform: uppercase;
  color: #fff;
  letter-spacing: -2px;
}

.marquee-plus {
  color: var(--accent-green);
  font-size: 4rem;
  font-weight: 300;
}

.divider-line {
  margin-top: 60px;
  position: relative;
  height: 1px;
  background: rgba(255, 255, 255, 0.1);
  display: flex;
  justify-content: center;
  align-items: center;
}

.star-center {
  background: var(--bg-dark);
  padding: 0 40px;
  color: var(--accent-green);
  font-size: 1.5rem;
  position: relative;
  z-index: 10;
}

@keyframes scroll {
  from { transform: translateX(0); }
  to { transform: translateX(-100%); }
}

@media (max-width: 768px) {
  .marquee-item { font-size: 3rem; gap: 30px; }
  .marquee-track { gap: 30px; }
  .marquee-plus { font-size: 2.5rem; }
}
</style>
