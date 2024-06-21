<template>
  <div class="back">

    <section class="about-me">
      <img src="../assets/Effects.png" class="effect" alt="Effects">
<<<<<<< HEAD
      <img src="../assets/barber-pole.svg" class="barber-pole" alt="">
      <img src="../assets/barber-pole.svg" class="barber-pole2" alt="">
      <div class="effect-lucas">
        <img src="../assets/barber-scissor.svg" class="scissor" alt="">
        <img src="../assets/barber-scissor.svg" class="scissor2" alt="">
        <img class="lucas-backdrop" src="../assets/LucaoPhoto.png" alt="Lucas Hoffmann">
=======
      <div class="center">

        <div class="effect-lucas">
          <img src="../assets/barber-scissor.svg" class="scissor" alt="">
          <img src="../assets/barber-scissor.svg" class="scissor2" alt="">
          <img class="lucas-backdrop" src="../assets/LucaoPhoto.png" alt="Lucas Hoffmann">
        </div>

        <div class="p">
          <h1><b> QUEM É LUCAS HOFFMANN?</b></h1>
          <p>Barbeiro a mais de 3 anos, mais de 4 certificados no currículo, um profissional capacitado para te atender!
            Alem de tudo, professor para barbeiro! Ministro cursos do iniciante ate as técnicas avançadas !</p>
        </div>
>>>>>>> a17cbc0a277e28d149b0ccee9f37bafd3e3abec5
      </div>
    </section>
    <section>
      <img src="../assets/Effect-invert.png" class="effect2" alt="Effects">
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

.effect2 {
  width: 100%;
  height: 800px;
  position: absolute;
}

.effect-lucas {
  position: relative;
  left: 9%;
  top: 15%;
  width: 15%;
  height: 50%;
}

.lucas-backdrop {
  position: relative;
  width: 100%;
  border-radius: 20px;
}

.scissor {
  width: 20%;
  position: absolute;
  top: 94%;
  left: -10%;
}

.scissor2 {
  width: 20%;
  position: absolute;
  top: -6%;
  left: 90%;
  rotate: 180deg;
}
<<<<<<< HEAD
.barber-pole {
  position: absolute;
  left: -1%;
  transform: scaleX(-1);
}
.barber-pole2 {
  position: absolute;
  right: 0%;
  margin-right: 0;
=======

.p {
  position: relative;
  color: #3E3E3E;
  left: 35%;
  top: 10%;
  text-align: center;
}

.p h1 {
  width: 50%;
  font-size: 42px;
  font-weight: 900;
}

.p p {
  width: 30%;
  left: 9.5%;
  position: relative;
  font-size: 120%;
}

@media(max-width: 970px) {

  .about-me {
    display: grid;
  }
  .p{
    justify-content: center;
  }
.p h1{
  font-size: 180%;
}
  .p p {
    font-size: 100%;
  }


>>>>>>> a17cbc0a277e28d149b0ccee9f37bafd3e3abec5
}
</style>