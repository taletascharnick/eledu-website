<template>
  <div id="app">
    <a href="#main-content" class="skip-link">Skip to main content</a>
    <NavBar />
    <main id="main-content">
      <HomeView />
    </main>
    <FooterSection />
  </div>
</template>

<script setup>
import NavBar from './components/NavBar.vue'
import FooterSection from './components/FooterSection.vue'
import HomeView from './views/HomeView.vue'
</script>

<style>
#app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

main {
  flex: 1;
}

.skip-link {
  position: absolute;
  top: -100%;
  left: 0.5rem;
  background: var(--color-primary);
  color: var(--color-on-primary);
  padding: 0.5rem 1.25rem;
  font-weight: 700;
  border-radius: 0 0 4px 4px;
  z-index: 9999;
  transition: top 0.1s;
}

.skip-link:focus {
  top: 0;
}
</style>
