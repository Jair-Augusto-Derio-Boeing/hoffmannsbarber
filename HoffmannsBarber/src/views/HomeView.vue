<template>
  <div class="back">

    <section class="about-me">

      <div class="effect"></div>

      <div class="effect-lucas">
        <img class="lucas-backdrop" src="../assets/backdrop-lucas.svg" alt="Lucas Hoffmann">
        <img class="lucas-shiny" src="../assets/lucas-blank.svg" alt="lucas Hoffmann Shiny">
      </div>

    </section>

    <Navbar></Navbar>
  </div>

  
</template>

<script>

import Navbar from '@/components/Navbar.vue';

export default {
  methods: {

  },
  components: {
    Navbar,
  },
}
</script>

<style>
.back {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 400vh;
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
  background-color: #D9D9D9;
  position: absolute;
  top: -50%;
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
</style>