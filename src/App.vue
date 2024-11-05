<script setup>
import { RouterView } from 'vue-router'
import { ref, provide, onMounted } from 'vue'

const isDarkMode = ref(false)

const switchTheme = () => {
  const rootElement = document.documentElement
  rootElement.setAttribute('data-bs-theme', isDarkMode.value ? 'dark' : 'light')
  localStorage.setItem('theme', isDarkMode.value ? 'dark' : 'light')
}

const initTheme = () => {
  const storedPreference = localStorage.getItem('theme')
  if (storedPreference) {
    isDarkMode.value = storedPreference === 'dark'
  } else if (window.matchMedia('(data-bs-theme: dark)').matches) {
    isDarkMode.value = true
  }
  switchTheme()
}

onMounted(() => {
  initTheme()
})

provide('isDarkMode', isDarkMode)
provide('switchTheme', switchTheme)
</script>

<template>
  <div>
    <DarkModeToggle />
    <RouterView />
  </div>
</template>
