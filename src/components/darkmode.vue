<script setup>
import { inject } from 'vue'
const isDarkMode = inject('isDarkMode')
const switchTheme = inject('switchTheme')
</script>

<template>
  <div id="darkmode-switch" class="btn-toggle-switch">
    <span class="label">Dark mode</span>
    <label class="switch toggle-switch" aria-label="darkmode switch">
      <input
        type="checkbox"
        name="checkbox"
        v-model="isDarkMode"
        @change="switchTheme"
      />
      <span class="slider round"></span>
    </label>
  </div>
</template>

<style scoped>
.label {
  display: none;
}
.switch {
  position: relative;
  display: inline-block;
  width: 60px;
  height: 24px;
}

/* Hide default HTML checkbox */
.switch input {
  opacity: 0;
  width: 0;
  height: 0;
}

/* The slider */
.slider {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #ccc;
  -webkit-transition: 0.4s;
  transition: 0.4s;
  box-shadow: 0px 8px 18px -8px rgba(99, 102, 241, 0.9);
}

.slider:before {
  position: absolute;
  content: '';
  height: 18px;
  width: 18px;
  left: 2px;
  bottom: 4px;
  background-color: white;
  -webkit-transition: 0.4s;
  transition: 0.4s;
  box-shadow: 0px 8px 18px -8px rgba(99, 102, 241, 0.9);
}

input:checked + .slider {
  background-color: #6366f1;
}

input:focus + .slider {
  box-shadow: 0 0 1px #6366f1;
}

input:checked + .slider:before {
  -webkit-transform: translateX(26px);
  -ms-transform: translateX(26px);
  transform: translateX(36px);
  box-shadow: 0px 8px 18px -8px rgba(99, 102, 241, 0.9);
}

/* Rounded sliders */
.slider.round {
  border-radius: 46px;
}

.slider.round:before {
  border-radius: 50%;
}

.btn-toggle-switch {
  display: flex;
  margin-right: 1rem;

  gap: 10px;
}

@media (min-width: 768px) {
  .label {
    display: block;
  }
}
</style>
