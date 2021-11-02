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
    /*Aclaración: ref retorna un objeto, y es por eso que dentro del script tengo que acceder
      a los valores con .value (power.value en este caso).
      Luego en el template ya no es necesario utilizarlo de esta forma. Simplemente ponemos power.
    */
    let power = ref(200);

    const upPower = () => {
      power.value++; //dentro del s
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
