<template>
  <div class="back">

    <section class="about-me">
      <img src="../assets/Effects.png" class="effect" alt="Effects">

      <img src="../assets/barber-pole.svg" class="barber-pole" alt="">
      <img src="../assets/barber-pole.svg" class="barber-pole2" alt="">
      <div class="center">

        <div style="display: grid;">
          <div class="effect-lucas">
            <img src="../assets/barber-scissor.svg" class="scissor" alt="">
            <img src="../assets/barber-scissor.svg" class="scissor2" alt="">
            <img class="lucas-backdrop" src="../assets/LucaoPhoto.png" alt="Lucas Hoffmann">
          </div>
          <div class="p">
            <h1>QUEM É LUCAS HOFFMANN?</h1>
            <p>Lucas Hoffman, Barbeiro a mais de 3 anos, possui mais de 4 certificados no currículo, um profissional
              capacitado para te atender!
              Além de tudo isso, Lucas ministra seu próprio curso de barbeiro, indo do iniciante até técnicas avançadas!
            </p>
          </div>
        </div>

      </div>
    </section>
    <section>
      <img src="../assets/Effect-invert.png" class="effect2" alt="Effects">
    </section>
    <Navbar v-model:NoneLogo="NoneLogo" @OpenMenu="OpenMenu"></Navbar>
    <Menu v-model:showMenu="showMenu"></Menu>
  </div>


</template>

<script>

import Navbar from '@/components/Navbar.vue';
import Menu from '@/components/Menu.vue'

export default {
  data() {
    return {
      showMenu: false,
    }
  },
  methods: {
    OpenMenu() {
      if (this.showMenu === true) {
        this.showMenu = false;
      }
      else {
        this.showMenu = true;
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
html {
  overflow-x: hidden;

}

.back {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  min-height: 100vh;
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
  width: 400px;
  height: 450px;
  bottom: 100px;
}

.lucas-backdrop {
  width: 100%;
  border-radius: 20px;

}

.scissor {
  width: 20%;
  position: relative;
  top: 450px;
  left: -35px;
}

.scissor2 {
  width: 20%;
  position: relative;
  top: 35px;
  left: 200px;
  rotate: 180deg;
}

.barber-pole {
  position: absolute;
  left: -1%;
  transform: scaleX(-1);
}

.barber-pole2 {
  position: absolute;
  right: -1%;
  margin-right: 0;
  bottom: 0;
}

.p {
  display: grid;
  position: relative;
  color: #3E3E3E;
  text-align: justify;
  width: 100%;
  font-size: 25px;
  justify-items: center;
}

.p p {
  width: 50%;
}

.p h1 {
  font-size: 42px;
  font-weight: 900;
}

.grid {
  display: flex;
  align-items: center;
  gap: 10%;
  margin-top: 150px;
  width: 100vw
}

@media(max-width: 970px) {
  .grid {
    display: grid;
    z-index: 10;
    justify-items: center;
  }

  .effect-lucas {
    width: 250px;
    height: 300px;
  }

  .center {
    display: grid;
    align-items: center;
  }
}
</style>