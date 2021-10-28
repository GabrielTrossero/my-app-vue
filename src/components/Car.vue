<template>
  <h2>Coche</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Potencias:</p>
  <!-- Tengo que poner el v-for dentro de un template para que no me
  muestre cada li (porque si lo evalua, ya lo muestra) -->
  <ul>
    <template v-for="(power, index) in powers" :key="index">
      <li v-if="power < 300">
        {{ "Urbana: " + power }}
      </li>
      <li v-else-if="power >= 300 && power <= 350">
        {{ "Hibrido: " + power }}
      </li>
      <li v-else>
        {{ "Carrera: " + power }}
      </li>
    </template>
  </ul>
  <p>Datos: {{ messaje.title + " - " + messaje.description }}</p>
</template>

<script>
export default {
  setup() {
    const brand = "Audi";
    const model = "A4";
    const powers = [220, 280, 350, 430, 550, 650];
    const messaje = {
      title: "Audi A4",
      description: "Se vende con 84 mil km",
    };

    return {
      brand,
      model,
      powers,
      messaje,
    };
  },
};
</script>

<style></style>
