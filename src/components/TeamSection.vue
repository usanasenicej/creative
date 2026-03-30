<template>
  <section class="team-section">
    <div class="container overflow-visible">
      <div class="team-header">
        <h2 class="section-title">Meet <span class="green-text pill">the Team</span></h2>
        <div class="header-actions">
          <button class="join-btn pill">Join Our Team <span class="arrow-up-right">↗</span></button>
        </div>
      </div>
      
      <div class="team-grid">
        <div v-for="(member, index) in team" :key="index" class="team-card pill">
          <div class="member-top">
            <div class="member-img-container">
              <img :src="member.image" :alt="member.name" class="member-img">
              <div class="img-badge">
                <div class="logo-mini"></div>
              </div>
            </div>
            <div class="member-info">
              <h3 class="member-name">{{ member.name }}</h3>
              <div class="role-row">
                <p class="member-role">{{ member.role }}</p>
                <div class="member-socials">
                  <span class="social-icon">in</span>
                  <span class="social-icon">𝕏</span>
                </div>
              </div>
            </div>
          </div>
          <div class="member-bottom">
            <p class="member-bio">{{ member.bio }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const team = [
  {
    name: 'John Doe',
    role: 'CEO & Founder',
    bio: '10 years of experience in creative leadership and business strategy.',
    image: 'https://images.unsplash.com/photo-1539571696357-5a69c17a67c6?auto=format&fit=crop&q=80&w=400'
  },
  {
    name: 'Alex Smith',
    role: 'Head of Operations',
    bio: 'Expert in streamlining workflows and ensuring project excellence.',
    image: 'https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?auto=format&fit=crop&q=80&w=400'
  },
  {
    name: 'Jane Smith',
    role: 'Lead UX Designer',
    bio: 'Focused on creating intuitive and accessible digital experiences.',
    image: 'https://images.unsplash.com/photo-1544005313-94ddf0286df2?auto=format&fit=crop&q=80&w=400'
  },
  {
    name: 'Zoe White',
    role: 'Art Director',
    bio: 'Award-winning designer with a passion for bold visuals.',
    image: 'https://images.unsplash.com/photo-1580489944761-15a19d654956?auto=format&fit=crop&q=80&w=400'
  },
  {
    name: 'Eva Miller',
    role: 'Lead Developer',
    bio: 'Turning designs into performant and reliable products.',
    image: 'https://images.unsplash.com/photo-1494790108377-be9c29b29330?auto=format&fit=crop&q=80&w=400'
  },
  {
    name: 'Liam Harris',
    role: 'Account Manager',
    bio: 'Passionate about building lasting client relationships.',
    image: 'https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?auto=format&fit=crop&q=80&w=400'
  }
]
</script>

<style scoped>
.team-section {
  background-color: var(--bg-dark);
  padding: 120px 0;
}

.team-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
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

.join-btn {
  background: #111;
  color: #fff;
  border: 1px solid rgba(255, 255, 255, 0.2);
  padding: 18px 36px;
  font-weight: 700;
  font-size: 1rem;
}

.join-btn:hover {
  background: var(--accent-green);
  color: #000;
  border-color: var(--accent-green);
}

.team-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 30px;
}

.team-card {
  background: #111;
  border: 1px solid rgba(255, 255, 255, 0.1);
  padding: 40px;
  display: flex;
  flex-direction: column;
  gap: 30px;
  transition: var(--transition);
  cursor: pointer;
}

.team-card:hover {
  transform: translateY(-10px);
  border-color: var(--accent-green);
  box-shadow: 0 30px 60px rgba(0, 0, 0, 0.6);
}

.member-top {
  display: flex;
  align-items: center;
  gap: 20px;
}

.member-img-container {
  position: relative;
  width: 100px;
  height: 100px;
}

.member-img {
  width: 100%;
  height: 100%;
  border-radius: 50%;
  object-fit: cover;
  border: 2px solid var(--accent-green);
  padding: 4px;
}

.img-badge {
  position: absolute;
  top: -5px;
  right: -5px;
  background: var(--accent-green);
  width: 30px;
  height: 30px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  border: 2px solid #111;
}

.logo-mini {
  width: 12px;
  height: 12px;
  background: #000;
  clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
}

.member-name {
  font-size: 1.4rem;
  font-weight: 800;
  color: #fff;
  margin-bottom: 4px;
}

.role-row {
  display: flex;
  align-items: center;
  gap: 15px;
}

.member-role {
  font-size: 0.9rem;
  color: var(--text-dim);
  text-transform: uppercase;
  letter-spacing: 1px;
}

.member-socials {
  display: flex;
  gap: 10px;
  opacity: 0;
  transform: translateX(-10px);
  transition: all 0.4s ease;
}

.team-card:hover .member-socials {
  opacity: 1;
  transform: translateX(0);
}

.social-icon {
  width: 24px;
  height: 24px;
  background: rgba(255, 255, 255, 0.1);
  color: #fff;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 0.75rem;
  font-weight: 800;
  transition: all 0.3s ease;
}

.social-icon:hover {
  background: var(--accent-green);
  color: #000;
  transform: scale(1.2);
}

.member-bio {
  font-size: 0.95rem;
  color: var(--text-dim);
  line-height: 1.5;
}

.arrow-up-right {
  font-size: 1.2rem;
  margin-left: 8px;
}

@media (max-width: 1024px) {
  .team-grid { grid-template-columns: repeat(2, 1fr); }
  .section-title { font-size: 2.5rem; }
}

@media (max-width: 768px) {
  .team-grid { grid-template-columns: 1fr; }
  .team-header { flex-direction: column; gap: 30px; align-items: flex-start; }
}
</style>
