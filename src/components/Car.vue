<template>
  <h2>Coche</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>color: {{ color[1] }}</p>
  <p>Precio: {{ price }}</p>
  <p>Potencia: {{ power }}</p>
  <p>Datos: {{ messaje.title + " - " + messaje.description }}</p>
</template>

<script>
export default {
  /* VERSION 2 DE VUE:
  data() {
    return {
      brand: "Audi",
      model: "A4",
      color: ["Azul", "Rojo", "Negro"],
      price: 39000,
      power: 250,
      messaje: {
        title: "Audi A4",
        description: "Se vende",
      },
    };
  },*/

  // VERSION 3 DE VUE:
  setup() {
    const brand = "Audi";
    const model = "A4";
    const color = ["Azul", "Rojo", "Negro"];
    const price = 39000;
    const power = 250;
    const messaje = {
      title: "Audi A4",
      description: "Se vende",
    };

    return {
      brand,
      model,
      color,
      price,
      power,
      messaje,
    };
  },
};
</script>

<style></style>
