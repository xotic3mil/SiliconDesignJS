<script setup>
import { ref, onMounted } from 'vue'

let testimonials = ref([])

onMounted(() => {
  fetch('https://win24-assignment.azurewebsites.net/api/testimonials')
    .then(response => response.json())
    .then(data => {
      testimonials.value = data
      console.log(testimonials.value)
    })
    .catch(error => {
      console.error('Error fetching testimonials:', error)
    })
})
</script>
<template>
  <section class="page-5">
    <br /><br />
    <div class="page-5-container">
      <div class="paper-container">
        <h2>Clients Are Loving Our App</h2>
        <article
          v-for="(testimonial, index) in testimonials"
          :key="index"
          :class="['paper-', 'paper-' + (index + 1)]"
          :id="'customer-' + (index + 1)"
        >
          <div class="bg">
            <div class="quotes">
              <img src="/media/quotes.svg" alt="Quotes" />
            </div>
            <div class="rating">
              <img
                v-for="starIndex in testimonial.starRating"
                :key="starIndex"
                src="/images/star.svg"
                alt="Star"
              />
            </div>
            <p class="review">{{ testimonial.comment }}</p>
            <img
              :src="testimonial.avatarUrl"
              :alt="`Portrait of ${testimonial.name}`"
            />
            <div class="paper-customer">
              <strong>{{ testimonial.author }}</strong>
              <p>{{ testimonial.jobRole }}</p>
            </div>
          </div>
        </article>
      </div>
    </div>
    <br /><br />
  </section>
</template>
<style scoped>
.page-5 {
  display: none;

  .page-5-container {
    display: none;
  }
}

.paper-container {
  display: grid;
  grid-template-columns: repeat(12, minmax(0, 1fr));

  h2 {
    grid-column: 1/4;
  }

  .paper-1 {
    position: relative;
    display: grid;
    grid-column: 5/6;
    grid-row: 1/2;
    width: 416px;

    .quotes {
      position: absolute;
      top: -15px;
      left: 40px;
      display: flex;
      width: 44px;
      height: 44px;
      justify-content: center;
      align-items: center;
      flex-shrink: 0;
      border-radius: 6px;
      background: #6366f1;
      box-shadow: 0px 8px 18px -8px rgba(99, 102, 241, 0.9);
    }
  }

  .paper-2 {
    position: relative;
    display: grid;
    grid-column: 9/10;
    grid-row: 1/2;
    width: 416px;

    .quotes {
      position: absolute;
      top: -15px;
      left: 40px;
      display: flex;
      width: 44px;
      height: 44px;
      justify-content: center;
      align-items: center;
      flex-shrink: 0;
      border-radius: 6px;
      background: #6366f1;
      box-shadow: 0px 8px 18px -8px rgba(99, 102, 241, 0.9);
    }
  }

  .rating {
    margin-bottom: 1rem;
  }

  .review {
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: 160%;
  }

  h6 {
    margin: 0px 0px;
  }
}

@media (min-width: 768px) {
  .page-5 {
    display: none;
  }
}

@media (min-width: 1400px) {
  .page-5 {
    display: block;

    background-color: var(--Gray-100);

    .page-5-container {
      max-width: 1320px;
      margin: 0 auto;
      display: block;
    }
  }

  .bg {
    padding: 48px 24px 24px 24px;
    border-radius: 8px;
    box-shadow:
      0px 4.4px 12px -1px rgba(19, 16, 34, 0.06),
      0px 2px 6.4px -1px rgba(19, 16, 34, 0.03);
    background: var(--White, #fff);
  }
}
</style>
