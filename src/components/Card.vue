<template>
  <div class="d-flex container-fluid justify-content-around mt-5">
    <div v-for="(i, index) in cards" :key="index" class="">
      <div class="card" style="width: 18rem">
        <img src="..." class="card-img-top" alt="..." />
        <div class="card-body">
          <h5 class="card-title">{{ i.titulo }}</h5>
          <p class="card-text">
            Some quick example text to build on the card title and make up the
            bulk of the card's content.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const cards = [
  {
    icono: "icono",
    titulo: "Item 1",
    contenido: "titulo",
  },
  {
    icono: "icono",
    titulo: "Item 2",
    contenido: "titulo",
  },
  {
    icono: "icono",
    titulo: "Item 3",
    contenido: "titulo",
  },
];
</script>