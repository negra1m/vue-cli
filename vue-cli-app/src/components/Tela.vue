<template>
  <div>
    <h1>{{msg}}</h1>
    <h3 v-text="titulo"></h3>
  </div>
</template>

<script>
export default {
  name: "Tela",
  //data contem todas as propriedades que serao manipuladas dentro desse mesmo componente
  data() {
    return {
      titulo: "Title"
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
