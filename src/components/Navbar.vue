<template>
  <nav class="navbar-wrapper">
    <div class="navbar-container pill glass">
      <ul class="nav-links left">
        <li><a href="#about" class="nav-link">About Us</a></li>
        <li><a href="#services" class="nav-link">Services</a></li>
      </ul>
      
      <div class="logo">
        <div class="logo-icon"></div>
        <span class="logo-text">Creatix</span>
      </div>
      
      <ul class="nav-links right">
        <li><a href="#projects" class="nav-link">Projects</a></li>
        <li><a href="#reviews" class="nav-link">Reviews</a></li>
      </ul>
    </div>
  </nav>
</template>

<style scoped>
.navbar-wrapper {
  position: fixed;
  top: 30px;
  left: 0;
  right: 0;
  z-index: 1000;
  display: flex;
  justify-content: center;
  padding: 0 20px;
}

.navbar-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 12px 40px;
  width: auto;
  min-width: 600px;
  max-width: 900px;
  gap: 60px;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);
}

.nav-links {
  display: flex;
  gap: 30px;
  width: 250px;
}

.nav-links.left { justify-content: flex-end; }
.nav-links.right { justify-content: flex-start; }

.nav-link {
  font-size: 0.9rem;
  font-weight: 500;
  color: var(--text-main);
  opacity: 0.8;
  letter-spacing: 0.5px;
}

.nav-link:hover {
  opacity: 1;
  color: var(--accent-green);
}

.logo {
  display: flex;
  align-items: center;
  gap: 10px;
  cursor: pointer;
}

.logo-icon {
  width: 24px;
  height: 24px;
  background-color: var(--accent-green);
  clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
  animation: rotateLogo 8s linear infinite;
}

@keyframes rotateLogo {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}

.logo-text {
  font-size: 1.4rem;
  font-weight: 800;
  letter-spacing: -1px;
}

@media (max-width: 768px) {
  .navbar-container {
    min-width: 90vw;
    padding: 10px 20px;
    gap: 20px;
  }
  
  .nav-link {
    font-size: 0.8rem;
  }
  
  .nav-links {
    gap: 15px;
    width: auto;
  }
}
</style>
