<!-- Version 3 Vue-->
<!-- Archivo para ver la diferencia de la estructura entre
    un archivo de la version 2 y la 3 -->
<template>
  <h2>Coche - Composition API</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Potencia: {{ power }}</p>
  <button @click="upPower(20)">Aumentar</button>
  <button @click="downPower">Disminuir</button>
</template>

<script>
//ref me sirve para que el valor de power cambie dinamicamente en la vista
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
