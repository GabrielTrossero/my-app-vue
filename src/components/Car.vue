<!-- Version 3 Vue-->
<template>
  <h2>Coche - Composition API</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Potencia: {{ power }}</p>
</template>

<script>
export default {
  props: {
    power: {
      type: Number,
      default: 250, //si no recibo nada, seteo que sea 250
    },
  },

  setup(props) {
    const brand = "Audi";
    const model = "A4";

    console.log(props.power);

    return {
      brand,
      model,
    };
  },
};
</script>

<style></style>
