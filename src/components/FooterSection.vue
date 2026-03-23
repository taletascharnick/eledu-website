<template>
  <footer class="footer">
    <div class="footer__container">
      <div class="footer__brand">
        <img src="../assets/logo.png" alt="EL Education Logo" class="footer__logo" />
        <span class="footer__name">EL Education</span>
      </div>

      <p class="footer__tagline">
        Passionate about teaching. Passionate about accounting.
      </p>

      <div class="footer__contact">
        <a href="mailto:eleducation2021@gmail.com" class="footer__email">
          eleducation2021@gmail.com
        </a>
      </div>

      <p class="footer__copy">
        &copy; {{ new Date().getFullYear() }} EL Education. All rights reserved.
      </p>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background-color: var(--color-surface);
  color: #aaa;
  padding: 2rem 1rem;
  text-align: center;
}

@media (min-width: 641px) {
  .footer {
    padding: 2.5rem 1.5rem;
  }
}

.footer__container {
  max-width: 800px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
}

.footer__brand {
  display: flex;
  align-items: center;
  gap: 0.6rem;
}

.footer__logo {
  height: 40px;
  width: auto;
  border-radius: 4px;
}

.footer__name {
  font-size: 1.1rem;
  font-weight: 700;
  color: #fff;
}

.footer__tagline {
  font-size: 0.9rem;
  font-style: italic;
}

.footer__email {
  color: #ff7c79;
  font-weight: 600;
  font-size: 0.95rem;
  transition: color 0.2s;
}

.footer__email:hover {
  color: #ffb3b1;
}

.footer__copy {
  font-size: 0.8rem;
  color: #999;
}
</style>
