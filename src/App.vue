<template>
  <h1>Vue JS</h1>
  <CarOptions />
  <hr />
  <CarComposition />
</template>

<script>
import CarOptions from "./components/CarOptions.vue";
import CarComposition from "./components/CarComposition.vue";

export default {
  components: {
    CarOptions,
    CarComposition,
  },
};
</script>

<style></style>
