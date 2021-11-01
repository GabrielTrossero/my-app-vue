<template>
  <h1>Vue JS</h1>
  <Car :power="power" :upPower="upPower" :downPower="downPower" />
</template>

<script>
import Car from "./components/Car.vue";
import { ref } from "vue"; //ref me sirve para que el valor de power cambie dinamicamente en la vista

export default {
  components: {
    Car,
  },

  setup() {
    let power = ref(200);

    const upPower = () => {
      power.value++;
    };

    const downPower = () => {
      power.value--;
    };

    return {
      power,
      upPower,
      downPower,
    };
  },
};
</script>

<style></style>
