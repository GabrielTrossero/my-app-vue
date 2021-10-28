<template>
  <h2>Coche</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Color:</p>
  <!-- Uso como índice al propio color, pero si uno se repite, ya no sería único
  <ul>
    <li v-for="color in colors" :key="color">
      {{ color }}
    </li>
  </ul>
  -->
  <ul>
    <!-- Genero un índice único -->
    <li v-for="(color, index) in colors" :key="index">
      {{ index + ": " + color }}
    </li>
  </ul>
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
    const colors = ["Azul", "Rojo", "Negro"];
    const price = 39000;
    const power = 250;
    const messaje = {
      title: "Audi A4",
      description: "Se vende",
    };

    return {
      brand,
      model,
      colors,
      price,
      power,
      messaje,
    };
  },
};
</script>

<style></style>
