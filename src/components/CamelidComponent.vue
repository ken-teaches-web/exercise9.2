<script setup>
const props = defineProps(["animal"]);
</script>
<template>
  <div class="card">
    <h3>{{ props.animal.commonName }}</h3>
    <small>binomial name: {{ props.animal.binomialName }}</small>
    <p>order: {{ props.animal.order }}</p>
    <p>family: {{ props.animal.family }}</p>
    <p>genus: {{ props.animal.genus }}</p>
    <p>species {{ props.animal.species }}</p>
    <img v-bind:src="props.animal.image" v-bind:alt="props.animal.commonName" />
  </div>
</template>
<style scoped>
.card {
  border: 1px solid #333;
  border-radius: 4px;
  width: 220px;
  padding: 10px;
  display: flex;
  flex-direction: column;
}
img {
  max-width: 200px;
}
</style>