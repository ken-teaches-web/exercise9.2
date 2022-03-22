<script setup>
import CamelidComponent from "./components/CamelidComponent.vue";
// javascript
const camelids = [
  {
    commonName: "Lama",
    binomialName: "Lama glama",
    order: "Artiodactyla",
    family: "Camelidae",
    genus: "Lama",
    species: "L. glama",
    image:
      "https://upload.wikimedia.org/wikipedia/commons/thumb/b/b9/Llama_lying_down.jpg/220px-Llama_lying_down.jpg",
  },
  {
    commonName: "Alpaca",
    binomialName: "Vicugna pacos",
    order: "Artiodactyla",
    family: "Camelidae",
    genus: "Vicugna",
    species: "V. pacos",
    image:
      "https://upload.wikimedia.org/wikipedia/commons/thumb/d/db/Alpaca_%2831562329701%29.jpg/440px-Alpaca_%2831562329701%29.jpg",
  },
];
</script>

<template>
  <!-- html -->
  <h1>My favorite Camelids</h1>
  <div class="camelids-wrapper">
    <CamelidComponent
      v-for="animal in camelids"
      v-bind:key="animal.commonName"
      v-bind:animal="animal"
    />
  </div>
</template>

<style>
/* css */
h1 {
  text-align: center;
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
  font-size: 64px;
}
.camelids-wrapper {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
}
</style>
