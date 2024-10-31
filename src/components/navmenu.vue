<script setup>
import darkmode from '../components/darkmode.vue'
</script>
<template>
  <header class="gloss">
    <div class="ctn">
      <div class="logo">
        <img src="../../media/logo.svg" alt="Logo" />
        <a class="nav-ft" href="/">Silicon</a>
      </div>
      <darkmode />
      <div class="nav-ft-wrap">
        <div class="hamburger" @click="toggleMenu">
          <span :class="{ open: isOpen }"></span>
          <span :class="{ open: isOpen }"></span>
          <span :class="{ open: isOpen }"></span>
        </div>
        <nav :class="{ navbar: true, open: isOpen }">
          <div>
            <a class="nav-ft" href="#">Features</a>
            <a class="nav-ft" href="/contact">Contact</a>
          </div>
          <button class="btn-primary" id="auth">Sign in / Up</button>
        </nav>
      </div>
    </div>
  </header>
</template>

<script scoped>
export default {
  data() {
    return {
      isOpen: false,
    }
  },
  methods: {
    toggleMenu() {
      this.isOpen = !this.isOpen
    },
  },
}
</script>

<style scoped>
header.gloss {
  position: sticky;
  top: 0;
  z-index: 10;
  background: rgba(255, 255, 255, 0);
  box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
  backdrop-filter: blur(3.5px);
  -webkit-backdrop-filter: blur(3.5px);
  border: 1px solid rgba(255, 255, 255, 0.18);
  border-radius: 2px;
  padding-left: 0.5rem;
  padding-right: 0.5rem;
  margin-bottom: 5rem;
}

.btn-primary {
  border: 0px;
  margin-right: 1rem;
  cursor: pointer;
}

.ctn {
  display: flex;
  justify-content: start;
  align-items: center;
  gap: 1.5rem;
  padding-top: 0.5rem;
  padding-bottom: 0.5rem;
}

.logo {
  grid-column: 1;
  color: #131022;
  font-size: 21.4px;
  font-style: normal;
  font-weight: 800;
  line-height: 34.16px;
}

.logo img {
  height: 40px;
  margin-right: 10px;
}

.hamburger {
  display: none;
  flex-direction: column;
  cursor: pointer;
}

.hamburger span {
  width: 25px;
  height: 3px;
  background-color: white;
  margin: 5px 0;
  transition: all 0.3s ease;
}

.hamburger span.open:nth-child(1) {
  transform: rotate(45deg) translate(5px, 5px);
}

.hamburger span.open:nth-child(2) {
  opacity: 0;
}

.hamburger span.open:nth-child(3) {
  transform: rotate(-45deg) translate(5px, -5px);
}

.navbar {
  display: flex;
  align-items: center;
  transition: all 0.3s ease;
}

.navbar.open {
  display: flex;
  padding-left: 10px;
  padding-right: 10px;
  position: absolute;
  top: 100%;
  width: 100%;
  right: 0;
  background: rgba(255, 255, 255, 0);
  box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
  backdrop-filter: blur(3.5px);
  -webkit-backdrop-filter: blur(3.5px);
  text-align: center;
}

.nav-ft {
  color: black;
  margin-right: 20px;
  text-decoration: none;
}

.nav-ft-wrap {
  display: flex;
}

#auth {
  background-color: #0066ff;
  color: white;
  padding: 10px 20px;
  max-width: 150px;
  text-decoration: none;
  border-radius: 5px;
}

@media (max-width: 768px) {
  .hamburger {
    display: flex;
  }

  .navbar {
    display: none;
  }

  .navbar.open {
    display: flex;
    top: 120%;
  }

  #auth {
    display: block;
    margin-top: 10px;
  }
}
</style>
