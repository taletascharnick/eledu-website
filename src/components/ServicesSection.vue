<template>
  <section id="services" class="services" aria-labelledby="services-heading">
    <div class="services__container">
      <div class="services__badge">Services</div>
      <h2 id="services-heading" class="services__title">What We Offer</h2>
      <p class="services__intro">
        Elsa provides one-on-one Accounting tutoring for high school learners
        across schools in George, tailoring each session to the individual
        learner's needs.
      </p>

      <div class="services__grid">
        <div v-for="service in services" :key="service.title" class="services__card">
          <span class="services__icon" aria-hidden="true">{{ service.icon }}</span>
          <h3 class="services__card-title">{{ service.title }}</h3>
          <p class="services__card-desc">{{ service.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const services = [
  {
    icon: '📘',
    title: 'One-on-One Tutoring',
    description:
      'Personalised lessons focused on the learner\'s unique strengths and gaps, ensuring steady progress.',
  },
  {
    icon: '📝',
    title: 'Exam Preparation',
    description:
      'Targeted revision and exam technique practice to help learners perform confidently under pressure.',
  },
  {
    icon: '⚖️',
    title: 'Accounting Fundamentals',
    description:
      'Building solid foundations in bookkeeping, financial statements, and accounting principles.',
  },
  {
    icon: '📊',
    title: 'Grade 10 – 12 Coverage',
    description:
      'Full CAPS Accounting curriculum support from Grade 10 through to Matric final exams.',
  },
]
</script>

<style scoped>
.services {
  padding: 2.5rem 1rem;
  background-color: #f9f9f9;
}

.services__container {
  max-width: 1000px;
  margin: 0 auto;
}

.services__badge {
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

.services__title {
  font-size: 1.5rem;
  font-weight: 800;
  color: var(--color-text);
  margin-bottom: 0.75rem;
}

.services__intro {
  color: #444;
  font-size: 1rem;
  max-width: 680px;
  margin-bottom: 2.5rem;
  line-height: 1.7;
}

.services__grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 1.25rem;
}

.services__card {
  background-color: var(--color-background);
  border: 2px solid #f0f0f0;
  border-radius: 10px;
  padding: 1.75rem 1.5rem;
  transition: border-color 0.2s, box-shadow 0.2s;
}

.services__card:hover {
  border-color: var(--color-primary);
  box-shadow: 0 4px 18px rgba(232, 69, 60, 0.12);
}

.services__icon {
  font-size: 2rem;
  display: block;
  margin-bottom: 0.75rem;
}

.services__card-title {
  font-size: 1.05rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: 0.5rem;
}

.services__card-desc {
  font-size: 0.9rem;
  color: #444;
  line-height: 1.7;
}

@media (min-width: 601px) {
  .services {
    padding: 4rem 1.5rem;
  }

  .services__title {
    font-size: 2rem;
  }

  .services__grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 1.5rem;
  }
}
</style>
