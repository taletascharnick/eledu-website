<template>
  <section class="hero" id="home" aria-label="Introduction">
    <div class="hero__container">
      <div class="hero__content">
        <h1 class="hero__title">
          Balancing Knowledge,<br>
          <span class="hero__highlight">Empowering Learners</span>
        </h1>

        <p class="hero__subtitle">
          Over 40 years of accounting expertise helping high school learners in George succeed.
        </p>

        <div class="hero__actions">
          <a href="#contact" class="btn btn--primary">Contact me</a>
        </div>
      </div>

      <div class="hero__visual">
        <img src="../assets/logo.png" alt="EL Education Logo" class="hero__logo" />
      </div>
    </div>
  </section>
</template>

<script setup>
// No script needed for static content
</script>

<style scoped>
.hero {
  background: linear-gradient(135deg, var(--color-surface) 0%, #2a2a2a 100%);
  color: #fff;
  padding: 3rem 1rem 4rem;
  position: relative;
  overflow: hidden;
}

.hero::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: radial-gradient(circle at 20% 80%, rgba(232, 69, 60, 0.1) 0%, transparent 50%),
              radial-gradient(circle at 80% 20%, rgba(192, 57, 43, 0.1) 0%, transparent 50%);
}

.hero__container {
  max-width: 1100px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr;
  gap: 2rem;
  align-items: center;
  text-align: center;
  position: relative;
  z-index: 1;
}

.hero__content {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.hero__title {
  font-size: clamp(2rem, 5vw, 3.5rem);
  font-weight: 800;
  line-height: 1.1;
  margin-bottom: 0.5rem;
}

.hero__highlight {
  color: var(--color-primary-dark);
}

.hero__subtitle {
  font-size: 1rem;
  color: #ccc;
  max-width: 500px;
}

.hero__actions {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
  justify-content: center;
}

.btn {
  display: inline-block;
  padding: 0.75rem 1.5rem;
  border-radius: 6px;
  font-weight: 600;
  text-align: center;
  transition: all 0.2s;
  border: 2px solid transparent;
}

.btn--primary {
  background-color: var(--color-primary);
  color: var(--color-on-primary);
  border-color: var(--color-primary);
}

.btn--primary:hover {
  background-color: var(--color-primary-dark);
  border-color: var(--color-primary-dark);
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(232, 69, 60, 0.3);
}

.btn--secondary {
  background-color: transparent;
  color: #fff;
  border-color: #666;
}

.btn--secondary:hover {
  background-color: #333;
  border-color: #999;
  transform: translateY(-2px);
}

.hero__visual {
  display: flex;
  justify-content: center;
  align-items: center;
}

.hero__logo {
  width: 100%;
  max-width: 180px;
  height: auto;
  filter: drop-shadow(0 8px 16px rgba(0, 0, 0, 0.4));
}

@media (min-width: 769px) {
  .hero {
    padding: 4rem 1.5rem 6rem;
  }

  .hero__container {
    grid-template-columns: 1fr 1fr;
    gap: 3rem;
    text-align: left;
  }

  .hero__subtitle {
    font-size: 1.2rem;
  }

  .hero__actions {
    justify-content: flex-start;
  }

  .hero__logo {
    max-width: 300px;
  }
}
</style>
