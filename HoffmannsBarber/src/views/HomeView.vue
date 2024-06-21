<template>
  <div class="back">

    <section class="about-me">

      <img src="../assets/Effects.png" class="effect" alt="Effects">


      <div class="effect-lucas">
        <img class="lucas-backdrop" src="../assets/backdrop-lucas.svg" alt="Lucas Hoffmann">
        <img class="lucas-shiny" src="../assets/lucas-blank.svg" alt="lucas Hoffmann Shiny">
      </div>

      <div class="p">
        <h1><b> QUEM É LUCAS HOFFMANN?</b></h1>
        <p>Barbeiro a mais de 3 anos, mais de 4 certificados no currículo, um profissional capacitado para te atender!
          Alem de tudo, professor para barbeiro! Ministro cursos do iniciante ate as técnicas avançadas !</p>
      </div>
    </section>

    <Navbar v-model:NoneLogo="NoneLogo" @OpenMenu="OpenMenu"></Navbar>
    <Menu v-model:ShowMenu="ShowMenu"></Menu>
  </div>


</template>

<script>

import Navbar from '@/components/Navbar.vue';
import Menu from '@/components/Menu.vue'

export default {
  data() {
    return {
      ShowMenu: false,
      NoneLogo: true,
    }
  },
  methods: {
    OpenMenu() {
      if (this.ShowMenu === true) {
        this.ShowMenu = false;
        this.NoneLogo = true;

      }
      else {
        this.ShowMenu = true;
        this.NoneLogo = false;

      }
    },
  },
  components: {
    Navbar,
    Menu,
  },
}
</script>

<style>
.back {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  min-height: 400vh;
  display: flex;
  flex-direction: column;
}

.about-me {
  position: relative;
  height: 88vh;
  width: 100%;
  background-color: white;

}

.effect {
  width: 100%;
  height: 800px;
  position: absolute;
}

.effect-lucas {
  position: relative;
  margin-top: 5%;
  margin-left: 10%;
}

.lucas-backdrop {
  position: absolute;
  width: 15%;
}

.lucas-shiny {
  position: absolute;
  filter: drop-shadow(1px 1px 10px white);
  top: -33px;
  left: -33px;
  width: 19%;
}

.scissors {
  width: 60px;
}

.p {
  position: relative;
  color: #3E3E3E;
  left: 35%;
  top: 10%;
  text-align: center;
}
.p h1{
  width: 50%;
  font-size: 42px;
  font-weight: 900;
}
.p p{
  width: 30%;
  left: 9.5%;
  position: relative;
  font-size: 120%;
}
@media(max-width: 970px){
  
  .about-me{
    display: grid;
  }
  .p p{
  font-size: 100%;
}
}
</style>