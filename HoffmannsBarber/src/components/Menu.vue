<template>
  <div class="container" v-if="showMenu">
    <ul class="menu-list">
      <li class="item-list">Home</li>
      <li class="item-list">Catálogo</li>
      <li class="item-list">Planos</li>
      <li class="item-list">Contato</li>
    </ul>
    <img class="logo1" src="../assets/logo-blank.svg">
  </div>
</template>

<script>
export default {
  props: {
    showMenu: {
      type: Boolean,
      required: true
    },

  },
  methods: {

  },
}
</script>

<style>
.container {
  z-index: 9999;
  background-color: #002445;
  display: flex;
  flex-direction: column;
  position: fixed;
  width: 30%;
  height: 100vh;
  top: 0;
  left: 0;
  align-items: center;
  justify-content: center;
  transition: 0.3s ease-in;
  justify-content: space-between;
}

.menu-list {
  display: flex;
  list-style: none;
  align-items: center;
  flex-direction: column;
  gap: 50px;
  position: relative;
  top: 20%;
}

.item-list {
  text-decoration: none;
  font-size: 18px;
  color: black;
  font-weight: 600;
  transition: 0.3s;
  cursor: pointer;
}

.item-list:hover {
  color: white;
  transform: scale(1.1);
}

.logo1 {
  position: relative;
  left: 2%;
  bottom: 2%;
  filter: drop-shadow(1px 1px 4px white);
  transition: 0.3s;
  cursor: pointer;
}

.logo1:hover {
  filter: drop-shadow(3px 3px 10px white);
  transform: scale(1.1);
}
</style>