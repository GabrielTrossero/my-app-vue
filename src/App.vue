<template>
  <h1>Vue JS</h1>
  <Car :power="power" />
</template>

<script>
import Car from "./components/Car.vue";

export default {
  components: {
    Car,
  },

  setup() {
    let power = 200;

    return {
      power,
    };
  },
};
</script>

<style></style>
