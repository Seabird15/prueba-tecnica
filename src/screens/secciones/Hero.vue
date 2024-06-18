<template>
  <Nav />
  <div class="bg-black">
    <div
      class="bg-hero d-flex vh-100 flex-column align-items-center justify-content-center"
    >
      <div class="bg-title">
        <h1 class="fw-bold title text-center text-uppercase">
          Innovación a tu <strong>alcance</strong>
        </h1>
      </div>
      <div>
        <button type="button" class="button fw-bold text-uppercase">
          Enviar
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
import Nav from "../../components/Nav.vue";
</script>

<style>
.bg-black {
  background-image: url("../../assets/bg-hero.png");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}
.bg-hero {
  background-image: url("../../assets/shadow-bg.png");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}
.bg-title {
  background-color: rgba(255, 255, 255, 0.422);
  padding: 20px;
  border-radius: 20px;
  margin-bottom: 20px;
  width: 50%;
  color: white;
}
.bg-title:hover {
  background-color: white;
  transition: all 0.5s;
  color: #ca73c1;
}
.title {
  font-size: 48px;
  text-shadow: rgb(108, 108, 108) 2px 2px 2px;
  letter-spacing: 2px;
}
@media (max-width: 768px) {
  .title {
    font-size: 24px;
  }
  .bg-title {
    width: 80%;
  }
}

.button {
  background-color: rgb(191, 255, 0);
  padding: 10px 20px;
  border: none;
  border-radius: 10px;
  font-size: 20px;
  letter-spacing: 2px;
}
.button:hover {
  background-color: rgb(255, 255, 255);
  color: #ca73c1;
  transition: all 0.5s;
}
</style>
