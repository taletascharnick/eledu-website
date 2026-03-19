<template>
  <header class="navbar">
    <div class="navbar__container">
      <a href="#home" class="navbar__brand">
        <img src="../assets/logo.png" alt="EL Education Logo" class="navbar__logo" />
        <span class="navbar__name">EL Education</span>
      </a>

      <nav class="navbar__nav" aria-label="Primary navigation">
        <a href="#about"    class="navbar__link">About</a>
        <a href="#services" class="navbar__link">Services</a>
        <a href="#contact"  class="navbar__link navbar__link--cta">Contact</a>
      </nav>

      <button
        class="navbar__toggle"
        :aria-expanded="menuOpen.toString()"
        aria-controls="mobile-nav"
        aria-label="Toggle navigation"
        @click="menuOpen = !menuOpen"
      >
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
      </button>
    </div>

    <nav v-if="menuOpen" id="mobile-nav" class="navbar__mobile" aria-label="Mobile navigation">
      <a href="#about"    class="navbar__mobile-link" @click="menuOpen = false">About</a>
      <a href="#services" class="navbar__mobile-link" @click="menuOpen = false">Services</a>
      <a href="#contact"  class="navbar__mobile-link" @click="menuOpen = false">Contact</a>
    </nav>
  </header>
</template>

<script setup>
import { ref } from 'vue'
const menuOpen = ref(false)
</script>

<style scoped>
.navbar {
  position: sticky;
  top: 0;
  z-index: 100;
  background-color: var(--color-surface);
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.4);
}

.navbar__container {
  max-width: 1100px;
  margin: 0 auto;
  padding: 0.75rem 1.5rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

/* Brand */
.navbar__brand {
  display: flex;
  align-items: center;
  gap: 0.75rem;
}

.navbar__logo {
  height: 48px;
  width: auto;
  border-radius: 4px;
}

.navbar__name {
  font-size: 1.2rem;
  font-weight: 700;
  letter-spacing: 0.4px;
  color: var(--color-on-primary);
}

/* Desktop nav – hidden on mobile, shown on sm+ */
.navbar__nav {
  display: none;
  gap: 1.5rem;
  align-items: center;
}

.navbar__link {
  color: #ccc;
  font-size: 0.95rem;
  font-weight: 500;
  transition: color 0.2s;
}

.navbar__link:hover {
  color: #fff;
}

.navbar__link--cta {
  background-color: var(--color-primary);
  color: var(--color-on-primary);
  padding: 0.4rem 1.1rem;
  border-radius: 4px;
  transition: background-color 0.2s;
}

.navbar__link--cta:hover {
  background-color: var(--color-primary-dark);
  color: #fff;
}

/* Hamburger – shown on mobile, hidden on sm+ */
.navbar__toggle {
  display: flex;
  flex-direction: column;
  gap: 5px;
  background: none;
  border: none;
  cursor: pointer;
  padding: 4px;
}

.navbar__toggle span {
  display: block;
  width: 24px;
  height: 2px;
  background-color: #fff;
  border-radius: 2px;
}

/* Mobile drawer */
.navbar__mobile {
  display: flex;
  flex-direction: column;
  padding: 0.25rem 1.5rem 1rem;
  background-color: var(--color-surface);
}

.navbar__mobile-link {
  color: #ccc;
  padding: 0.65rem 0;
  font-size: 1rem;
  border-bottom: 1px solid #2e2e2e;
  transition: color 0.2s;
}

.navbar__mobile-link:last-child {
  border-bottom: none;
}

.navbar__mobile-link:hover {
  color: #fff;
}

@media (min-width: 641px) {
  .navbar__nav    { display: flex; }
  .navbar__toggle { display: none; }
}
</style>
