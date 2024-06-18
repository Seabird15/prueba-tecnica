<template>
  <div class="container-global">
    <Hero />
    <img src="../assets//Ellipse 1.png" alt="" class="adorno-1" />
    <img src="../assets/Ellipse 2.png" alt="" class="adorno-2" />
    <Details />
  </div>
</template>

<script setup>
import Hero from "./secciones/Hero.vue";
import Details from "./secciones/Details.vue";
</script>

<style>
.container-global {
  position: relative;
}
.adorno-1 {
  position: absolute;
  top: 50%;
  right: 0;
}

@media (max-width: 768px) {
  .adorno-1 {
    display: none;
  }
}
@media (max-width: 768px) {
  .adorno-1 {
    display: none;
  }
}
.adorno-2 {
  position: absolute;
  bottom: 0;
  left: 0;
}
</style>
