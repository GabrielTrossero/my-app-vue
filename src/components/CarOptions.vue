<!-- Version 2 Vue -->
<!-- Archivo para ver la diferencia de la estructura entre
    un archivo de la version 2 y la 3 -->
<template>
  <h2>Coche - Options API</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Potencia: {{ power }}</p>
  <button @click="upPower(20)">Aumentar</button>
  <button @click="downPower">Disminuir</button>
</template>

<script>
export default {
  data() {
    return {
      brand: "Audi",
      model: "A4",
      power: 220,
    };
  },
  methods: {
    upPower(newPower) {
      this.power += newPower;
    },
    downPower() {
      this.power--;
    },
  },
};
</script>

<style></style>
