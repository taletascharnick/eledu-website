<template>
  <section id="about" class="about" aria-labelledby="about-heading">
    <div class="about__container">
      <div class="about__badge">About</div>
      <h2 id="about-heading" class="about__title">Meet Elsa Lamprecht</h2>

      <div class="about__grid">
        <div class="about__text">
          <p>
            Elsa Lamprecht is an experienced Accounting tutor based in
            <strong>George</strong>, South Africa. With more than
            <strong>40 years of teaching experience</strong>, she has guided
            countless high school learners from various schools in the country and now in George towards a confident understanding of Accounting.
          </p>
          <p>
            Her passion for both teaching and the subject itself shines through
            in every lesson — making complex concepts accessible and giving
            learners the tools they need to succeed.
          </p>
          <p>
            Extra classes are held at her home in George, conveniently located
            near the <strong>PNA on York Street</strong> — easy to find and accessible
            for learners from across the area. The exact address is shared directly
            upon scheduling a visit.
          </p>
        </div>

        <div class="about__highlights">
          <div class="about__card">
            <span class="about__card-number" aria-hidden="true">40+</span>
            <span class="about__card-label">Years of experience</span>
          </div>
          <div class="about__card">
            <span class="about__card-number" aria-hidden="true">&#x2696;</span>
            <span class="about__card-label">Accounting specialist</span>
          </div>
          <div class="about__card">
            <span class="about__card-number" aria-hidden="true">&#x1F4CD;</span>
            <span class="about__card-label">Based in George</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about {
  padding: 2.5rem 1rem;
  background-color: var(--color-background);
}

.about__container {
  max-width: 1000px;
  margin: 0 auto;
}

.about__badge {
  display: inline-block;
  background-color: var(--color-primary);
  color: var(--color-on-primary);
  font-size: 0.8rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 1.5px;
  padding: 0.25rem 0.9rem;
  border-radius: 20px;
  margin-bottom: 0.75rem;
}

.about__title {
  font-size: 1.75rem;
  font-weight: 800;
  color: var(--color-text);
  margin-bottom: 1.5rem;
}

.about__grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 1.5rem;
  align-items: start;
}

.about__text {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  font-size: 1.05rem;
  color: #333;
  line-height: 1.8;
}

.about__highlights {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.about__card {
  background-color: var(--color-primary);
  color: var(--color-on-primary);
  border-radius: 8px;
  padding: 1.25rem 1.5rem;
  display: flex;
  align-items: center;
  gap: 1.75rem;
}

.about__card-number {
  font-size: 2rem;
  font-weight: 800;
  flex-shrink: 0;
  width: 4.5rem;
  text-align: center;
  line-height: 1;
  border-right: 2px solid rgba(255, 255, 255, 0.35);
  padding-right: 1.75rem;
}

.about__card-label {
  font-size: 1.3rem;
  font-weight: 600;
}

@media (min-width: 641px) {
  .about {
    padding: 4rem 1.5rem;
  }

  .about__title {
    font-size: 2rem;
    margin-bottom: 2rem;
  }

  .about__grid {
    grid-template-columns: 1fr 1fr;
    gap: 2.5rem;
  }
}
</style>
