<!-- Version 3 Vue-->
<template>
  <h2>Coche - Composition API</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Potencia: {{ power }}</p>

  <!-- LLamo directamente a la función del componente App -->
  <button @click="upPower">Aumentar</button>

  <button @click="modifyDownPower">Disminuir</button>
</template>

<script>
export default {
  props: {
    power: {
      type: Number,
      default: 250, //si no recibo nada, seteo que sea 250
    },
    upPower: Function,
    downPower: Function,
  },

  setup(props) {
    const brand = "Audi";
    const model = "A4";

    console.log(props.power);

    const modifyDownPower = () => {
      props.downPower(); //función definida en componente App
      console.log("La potencia se disminuyó");
    };

    return {
      brand,
      model,
      modifyDownPower,
    };
  },
};
</script>

<style></style>
