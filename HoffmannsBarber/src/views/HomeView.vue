<template>
  <div class="back">
    <section class="about-me"> 

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
    height: 90vh;
    width: 100%;
    background-color: black;
  }
</style>