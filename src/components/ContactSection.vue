<template>
  <section id="contact" class="contact" aria-labelledby="contact-heading">
    <div class="contact__container">
      <div class="contact__badge">Contact</div>
      <h2 id="contact-heading" class="contact__title">Get in Touch</h2>
      <p class="contact__intro">
        Interested in tutoring for your child? Reach out to Elsa directly by
        email and she will get back to you as soon as possible.
      </p>

      <div class="contact__card">
        <div class="contact__row">
          <span class="contact__icon" aria-hidden="true">✉️</span>
          <div>
            <p class="contact__label">Email</p>
            <a
              href="mailto:eleducation2021@gmail.com"
              class="contact__value contact__link"
            >
              eleducation2021@gmail.com
            </a>
          </div>
        </div>

        <div class="contact__row">
          <span class="contact__icon" aria-hidden="true">📍</span>
          <div>
            <p class="contact__label">Location</p>
            <p class="contact__value">George, Western Cape, South Africa</p>
          </div>
        </div>
      </div>

      <a href="mailto:eleducation2021@gmail.com" class="contact__cta">
        Send an Email
      </a>
    </div>
  </section>
</template>

<style scoped>
.contact {
  padding: 2.5rem 1rem;
  background-color: var(--color-primary);
  color: var(--color-on-primary);
}

.contact__container {
  max-width: 700px;
  margin: 0 auto;
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1.25rem;
}

.contact__badge {
  display: inline-block;
  background-color: rgba(255, 255, 255, 0.25);
  color: #fff;
  font-size: 0.8rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 1.5px;
  padding: 0.25rem 0.9rem;
  border-radius: 20px;
}

.contact__title {
  font-size: 1.5rem;
  font-weight: 800;
}

.contact__intro {
  font-size: 1rem;
  opacity: 0.9;
  max-width: 520px;
  line-height: 1.7;
}

.contact__card {
  background-color: rgba(0, 0, 0, 0.18);
  border-radius: 10px;
  padding: 1.25rem 1rem;
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 1.25rem;
  text-align: left;
}

.contact__row {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
}

.contact__icon {
  font-size: 1.4rem;
  margin-top: 0.1rem;
}

.contact__label {
  font-size: 0.78rem;
  text-transform: uppercase;
  letter-spacing: 1px;
  opacity: 0.75;
  margin-bottom: 0.2rem;
}

.contact__value {
  font-size: 1rem;
  font-weight: 600;
}

.contact__link {
  color: #fff;
  transition: opacity 0.2s;
}

.contact__link:hover {
  opacity: 0.8;
}

.contact__cta {
  background-color: var(--color-on-primary);
  color: var(--color-primary);
  font-weight: 700;
  font-size: 1rem;
  padding: 0.8rem 2.25rem;
  border-radius: 4px;
  transition: background-color 0.2s, color 0.2s;
  margin-top: 0.25rem;
}

.contact__cta:hover {
  background-color: var(--color-surface);
  color: #fff;
}

@media (min-width: 481px) {
  .contact {
    padding: 4rem 1.5rem;
  }

  .contact__title {
    font-size: 2rem;
  }

  .contact__card {
    padding: 1.75rem 2rem;
  }
}
</style>
