<template>
  <div>
    <h1>{{msg}}</h1>
    <h3 v-text="titulo"></h3>
    <p v-text="titulo + new Date().toLocaleStrin()"></p>

    <span v-if="seen">Mostra isso?</span>
  </div>
</template>

<script>
//data contem todas as propriedades que serao manipuladas dentro desse mesmo componente
export default {
  name: "Tela",
  data() {
    return {
      titulo: "Title",
      seen: true
    };
  },
  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
