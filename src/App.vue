<script setup>
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import StatsSection from './components/StatsSection.vue'
import PortfolioSection from './components/PortfolioSection.vue'
import ServicesSection from './components/ServicesSection.vue'
import MarqueeSection from './components/MarqueeSection.vue'
import TeamSection from './components/TeamSection.vue'
import ReviewSection from './components/ReviewSection.vue'
import FooterSection from './components/FooterSection.vue'
</script>

<template>
  <div class="main-app">
    <Navbar />
    <main>
      <Hero />
      <StatsSection />
      <PortfolioSection />
      <ServicesSection />
      <MarqueeSection />
      <TeamSection />
      <ReviewSection />
    </main>
    <FooterSection />
  </div>
</template>

<style>
.main-app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

main {
  flex-grow: 1;
}

/* Page transitions/animations */
section {
  padding: 100px 0;
  position: relative;
  overflow: hidden;
}

@media (max-width: 768px) {
  section {
    padding: 60px 0;
  }
}
</style>
