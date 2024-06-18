<template>
  <div class="d-flex container-fluid justify-content-around pt-5 pb-5">
    <div v-for="(i, index) in cards" :key="index" class="">
      <div class="card mt-4" style="width: 18rem">
        <i :class="i.icono"></i>
        <div class="card-body">
          <h5 class="card-title fs-2 text-center text-uppercase">
            {{ i.titulo }}
          </h5>
          <p class="card-text text-center">
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
    icono: "ri-rocket-2-fill icon",
    titulo: "Item 1",
    contenido: "titulo",
  },
  {
    icono: "ri-bard-fill icon",
    titulo: "Item 2",
    contenido: "titulo",
  },
  {
    icono: "ri-heart-2-fill icon",
    titulo: "Item 3",
    contenido: "titulo",
  },
];
</script>

<style scoped>
i {
  color: #9f3e95;
}
i:hover {
  color: #c87ec2;
  transition: all 0.5s;
  transform: scale(1.2);
}
.card-img-top {
  width: 40% !important;
  margin: 0 auto;
}
.card-title {
  font-weight: bold;
  color: #ff93f4 !important;
  letter-spacing: 2px;
}
.card {
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1) !important;
  border-radius: 20px !important;
}
.card:hover {
  box-shadow: 0 0 40px rgba(0, 0, 0, 0.2) !important;
  transition: all 0.5s;
}
.icon {
  font-size: 5rem;
  margin: 0 auto;
  rotate: 50deg;
}

@media (max-width: 768px) {
  .container-fluid {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
}
</style>
