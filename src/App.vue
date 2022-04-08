<template>
  <div id="app">
    <Navbar />
    <div class="container">
      <!-- <div class="row">
        <div
          class="col"
          v-for="personagem in personagensMarvel"
          :key="personagem.id">
          <Card :personagem="personagem" />
        </div>
      </div>
      <div
      class="row">
        <div class="col"
        v-for="personagem in personagensDC"
        :key="personagem.id">
         <Card :personagem="personagem" />
        </div>
      </div>
    </div> -->
    <router-view />
   </div>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import Card from "@/components/Card.vue";


export default {
  name: "App",
  components: {
    Navbar,
    Card,

  },
  data() {
    return {
      personagensMarvel: [
        {
          id: 1,
          name: "Hulk",
          about: "Esmaga e cresce... birll!",
          photo:
            "https://i2.wp.com/www.multarte.com.br/wp-content/uploads/2019/03/hulk-png-sem-fundo9.png",
        },
        {
          id: 2,
          name: "Homem de ferro",
          about: "Jarvis..",
          photo: "https://2.bp.blogspot.com/-AHg84snN08A/V1IL3sI_OJI/AAAAAAAAEDc/UC7ahFmU7z8_m9PauTq4rQwuwaSJpIVfgCLcB/s1600/homemdsafas.png",
        },
        {
          id: 3,
          name: "Thor",
          about: "Eu sou thor!..",
          photo: "https://imagensemoldes.com.br/wp-content/uploads/2020/08/Pose-Thor-PNG.png",
        },
      ],
      personagensDC: [
        {
          id: 4,
          name: "Superman",
          about: "Eu sou o superman!..",
          category: "dc",
          photo:
            "https://i.pinimg.com/474x/a5/4a/64/a54a640e1472797500d0c1cf2c34a711.jpg",
        },
        {
          id: 5,
          name: "Coringa",
          about: "Eu sou coringa...",
          photo: "https://imagensemoldes.com.br/wp-content/uploads/2020/12/Arte-para-Camiseta-Coringa.png",
        },
        {
          id: 6,
          name: "Batman",
          about: "Eu sou batman!..",
          photo: "https://i0.wp.com/multarte.com.br/wp-content/uploads/2019/02/225cb8d8d207377e490d39188781fc5b.png",
        },
      ],
    };
  },
};
</script>
