<template>
  <div>
    <h1>{{msg}}</h1>
    <h3 v-text="titulo"></h3>
    <p v-text="titulo + new Date().toLocaleString()"></p>
    <span v-if="seen">Mostra isso?</span>
    <img v-bind:src="photo.url" v-bind:alt="photo.alt" />
  </div>
</template>

<script>
//data contem todas as propriedades que serao manipuladas dentro desse mesmo componente
export default {
  name: "Tela",
  data() {
    return {
      titulo: "Title",
      seen: false,
      photo: {
        url:
          "https://encrypted-tbn2.gstatic.com/images?q=tbn:ANd9GcTwV4kVzT5McBdGSgqlVeRzubrNH_mOrrkKseDOGFURq20HmsrelEfMU7It",
        alt: "Doguinho"
      }
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
