<template>
  <!-- Navbar -->
  <nav class="navbar bg-nav">
    <div class="container-fluid">
      <img src="../assets/logo.png" class="pb-2 pt-2 logo" alt="" />
      <div class="text-uppercase nav-desktop">
        <a
          class="navbar-brand text-white"
          href="#"
          :class="{ active: activeLink === 'Inicio' }"
          @click="setActive('Inicio')"
          >Inicio</a
        >
        <a
          class="navbar-brand text-white"
          href="#"
          :class="{ active: activeLink === 'Seccion 1' }"
          @click="setActive('Seccion 1')"
          >Seccion 1</a
        >
        <a
          class="navbar-brand text-white"
          href="#"
          :class="{ active: activeLink === 'Seccion 2' }"
          @click="setActive('Seccion 2')"
          >Seccion 2</a
        >
      </div>
      <button
        class="navbar-toggler nav-btn"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
        @click="toggleNavbar"
      >
        <i class="ri-menu-2-line text-white fs-1"></i>
      </button>

      <!-- Elementos del menú -->
      <div
        class="menu-mobile collapse navbar-collapse"
        :class="{ show: isNavOpen }"
        id="navbarNav"
      >
        <div class="text-uppercase d-flex flex-column pt-5 pb-5">
          <a class="navbar-brand text-white pt-4" href="#">
            <i class="ri-home-line text-white"></i>
            Inicio
          </a>
          <a class="navbar-brand text-white pt-4" href="#">
            <i class="ri-gemini-line text-white"></i>
            Seccion 1</a
          >
          <a class="navbar-brand text-white pt-4" href="#">
            <i class="ri-rocket-line text-white"></i>
            Seccion 2</a
          >
        </div>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref } from "vue";

const isNavOpen = ref(false);

const toggleNavbar = () => {
  isNavOpen.value = !isNavOpen.value;
};
</script>

<style scoped>
.bg-nav {
  background-color: #ff93f4;
}
.logo {
  margin-left: 10px;
}
.logo:hover {
  transform: scale(1.2);
  transition: all ease-in-out 0.5s;
}
.navbar-brand {
  font-weight: bold !important;
  letter-spacing: 2px;
  font-size: 24px !important;
}
.nav-desktop a {
  position: relative;
  display: inline-block;
  padding-bottom: 5px;
  color: white;
  text-decoration: none;
}

.nav-desktop a::after {
  content: "";
  position: absolute;
  width: 0;
  height: 2px;
  display: block;
  margin-top: 5px;
  right: 0;
  background: white;
  transition: width 0.3s ease, right 0.3s ease;
}

.nav-desktop a:hover::after {
  width: 100%;
  right: 0;
}

.nav-desktop a.active::after {
  width: 100%;
  right: 0;
}

@media (min-width: 768px) {
  .menu-mobile {
    display: none;
  }
  .nav-btn {
    display: none;
  }
}
@media (max-width: 768px) {
  .nav-desktop {
    display: none;
  }
}
</style>
