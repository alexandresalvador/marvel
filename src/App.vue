<template>
  <div id="app">
    <Navbar />
    <div class="container">
      <div class="row">
        <div
          class="col"
          v-for="personagem in personagens"
          :key="personagem.id">
          <Card :personagem="personagem" />
        </div>
      </div>
    </div>
    <router-view />
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
      personagens: [
        {
          id: 1,
          name: "Hulk",
          about: "Esmaga e cresce... birll!",
          photo:
            "https://i2.wp.com/www.multarte.com.br/wp-content/uploads/2019/03/hulk-png-sem-fundo9.png?fit=674%2C1024&ssl=1",
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
    };
  },
};
</script>
