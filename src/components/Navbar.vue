<template>
  <nav class="navbar-wrapper">
    <div class="navbar-container pill">
      <div class="nav-section left">
        <a href="#about" class="nav-link">About Us</a>
        <a href="#services" class="nav-link">Services</a>
      </div>
      
      <div class="logo">
        <div class="logo-icon-container">
          <div class="logo-icon"></div>
        </div>
        <span class="logo-text">Creatix</span>
      </div>
      
      <div class="nav-section right">
        <a href="#projects" class="nav-link">Projects</a>
        <a href="#reviews" class="nav-link">Reviews</a>
      </div>
    </div>
  </nav>
</template>

<style scoped>
.navbar-wrapper {
  position: absolute;
  top: 30px;
  left: 0;
  right: 0;
  z-index: 1000;
  display: flex;
  justify-content: center;
  padding: 0 40px;
}

.navbar-container {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 18px 40px;
  width: 100%;
  max-width: 900px; /* Slimmer as per UI */
  background: #000;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);
  gap: 60px;
}

.nav-section {
  display: flex;
  gap: 40px;
}

.nav-link {
  font-size: 0.9rem;
  font-weight: 500;
  color: #fff;
  opacity: 0.6;
}

.nav-link:hover {
  opacity: 1;
  color: var(--accent-green);
}

.logo {
  display: flex;
  align-items: center;
  gap: 10px;
}

.logo-icon-container {
  width: 24px;
  height: 24px;
  background: var(--accent-green);
  clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
  display: flex;
  align-items: center;
  justify-content: center;
}

.logo-icon {
  width: 10px;
  height: 10px;
  background: #000;
  clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
}

.logo-text {
  font-size: 1.4rem;
  font-weight: 800;
  color: #fff;
  letter-spacing: -1px;
}

@media (max-width: 768px) {
  .navbar-container {
    max-width: 90%;
    gap: 20px;
    padding: 12px 20px;
  }
  .nav-section { display: none; }
}
</style>
