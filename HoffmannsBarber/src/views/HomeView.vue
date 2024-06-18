<template>
  <div class="back">
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
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>