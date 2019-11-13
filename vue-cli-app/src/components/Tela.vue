<template>
  <div>
    <h1>{{msg}}</h1>
    <h3 v-text="titulo"></h3>
    <p v-text="titulo + new Date().toLocaleString()"></p>
    <span v-if="seen">Mostra isso?</span>
    <!-- Todos os atributos podem ser linkados com o v-bind, alguns deles possuem modifiers e.g.: disabled -->
    <img v-bind:src="photo.url" v-bind:alt="photo.alt" />
    <ul>
      <li v-for="photo in photos" :key="photo.id">
        <img :src="photo.url" :alt="photo.alt" />
      </li>
    </ul>
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
      },
      photos: [
        {
          id: 0,
          url:
            "https://encrypted-tbn2.gstatic.com/images?q=tbn:ANd9GcTwV4kVzT5McBdGSgqlVeRzubrNH_mOrrkKseDOGFURq20HmsrelEfMU7It",
          alt: "Doguinho"
        },
        {
          id: 1,
          url:
            "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTOhmlmzV4-Sifx5BIc2SXeA-1CtZJf8jb8V_vPZyKbXIQJKU-rkxGO6OM",
          alt: "Gato"
        }
      ]
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
