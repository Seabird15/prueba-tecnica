<template>
  <Nav />
  <div
    class="bg-hero vw-100 d-flex flex-column align-items-center justify-content-center"
  >
    <div>
      <h1 class="text-white fw-bold fs-1">Título banner principal</h1>
    </div>
    <div>
      <button type="button" class="btn btn-warning">Enviar</button>
    </div>
  </div>
</template>

<script setup>
import Nav from "../../components/Nav.vue";
</script>

<style>
.bg-hero {
  background-image: url("../../assets/bg-hero.jpg");
  height: 574px;
}
</style>
