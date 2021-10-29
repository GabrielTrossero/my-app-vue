<!-- Version 3 Vue-->
<template>
  <h2>Coche - Composition API</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Potencia: {{ power }}</p>
  <button @click="upPower(20)">Aumentar</button>
  <button @click="downPower">Disminuir</button>
</template>

<script>
//Uso el ref para poder modificar el valor de power
import { ref } from "vue";

export default {
  setup() {
    const brand = "Audi";
    const model = "A4";
    let power = ref(220);

    const upPower = (newPower) => {
      power.value += newPower;
    };
    const downPower = () => {
      power.value--;
    };

    return {
      brand,
      model,
      power,
      upPower,
      downPower,
    };
  },
};
</script>

<style></style>
