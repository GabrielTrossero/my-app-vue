<!-- Version 2 Vue-->
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
