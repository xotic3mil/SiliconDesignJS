<script setup>
import { ref, onMounted } from 'vue'

let faq = ref([])

onMounted(() => {
  fetch('https://win24-assignment.azurewebsites.net/api/faq')
    .then(response => response.json())
    .then(data => {
      faq.value = data
      console.log(faq.value)
    })
    .catch(error => {
      console.error('Error fetching faq:', error)
    })
})
</script>
<template>
  <div
    class="accordion"
    v-for="(item, index) in faq"
    :key="index"
    :id="['accordionPanelsStayOpenExample' + (index + 1)]"
  >
    <div class="accordion-item" style="margin-bottom: 1rem">
      <h2 class="accordion-header">
        <button
          class="accordion-button collapsed"
          type="button"
          :data-bs-toggle="'collapse'"
          :data-bs-target="'#panelsStayOpen-collapse' + index"
          aria-expanded="false"
          :aria-controls="'panelsStayOpen-collapse' + index"
        >
          {{ item.title }}
        </button>
      </h2>
      <div
        :id="'panelsStayOpen-collapse' + index"
        class="accordion-collapse collapse"
      >
        <div class="accordion-body">{{ item.content }}</div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.accordion {
  font-family: 'manrope' !important;

  .accordion-item {
    border: none !important;
  }

  .accordion-body {
    padding: 1rem !important;
    font-size: 1rem !important;
  }

  .accordion-button {
    color: black !important;
    background-color: white !important;
    box-shadow:
      0px 4.4px 12px -1px rgba(19, 16, 34, 0.06),
      0px 2px 6.4px -1px rgba(19, 16, 34, 0.03) !important;
    font-weight: 800 !important;

    &:active {
      color: black !important;
      background-color: white !important;
    }

    &:not(.collapsed) {
      color: var(--bs-accordion-active-color);
      background-color: white !important;
    }

    &:focus {
      outline: none !important;
      background-color: white !important;
    }
  }
}

:root[data-bs-theme='dark'] {
  .accordion {
    .accordion-body {
      background: hsl(223, 39%, 7%) !important;
    }

    .accordion-button {
      background: hsla(223, 39%, 7%, 0.541) !important;
      color: #ffff !important;
      box-shadow:
        0px 4.4px 12px 0px rgba(255, 255, 255, 0.06),
        2px 2px 5px 2px rgba(255, 255, 255, 0.25) !important;
    }
  }
}
</style>
