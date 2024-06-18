<template>
  <div class="back">
    <section class="about-me"> 
      <div class="effect-lucas">
        <img class="lucas-shiny" src="../assets/lucas-blank.svg" alt="lucas Hoffmann Shiny">
        <img class="lucas-backdrop" src="../assets/backdrop-lucas.svg" alt="Lucas Hoffmann">
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

<style >
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
    height: 85vh;
    width: 100%;
    background-color: black;
  }
  .lucas-shiny {
    filter: drop-shadow(1px 1px 10px white);
  }
  
</style>