<template>
  <nav>
      <img class="logo" src="../assets/logo-blank.svg">
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">Catálogo</a></li>
      <li><a href="#">Planos</a></li>
      <li><a href="#">Contato</a></li>
    </ul>
    <img @click="OpenMenu" src="../assets/menu-hamburguer.svg" class="menu-hamburguer">
  </nav>
</template>

<script>

export default {
  props: {
  },
  methods: {
    OpenMenu() {
      this.$emit('OpenMenu');

    }
  },
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
nav {
  box-shadow: 0 7px 6px rgba(0, 0, 0, 0.2); 
  width: 100%;
  height: 12vh;
  background-color: #D9D9D9;
  position: sticky;
  top: 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
  z-index: 1000;
}

.menu-hamburguer {
  cursor: pointer;
  display: none;
  position: relative;
  right: 5%;
}

nav ul {
  display: flex;
  list-style: none;
  align-items: center;
}

nav ul li {
  padding: 0 40px 0 20px;
  transition: transform 0.3s ease-in-out ;
}
nav ul li:hover {
  transform: scale(1.1);
  filter: drop-shadow(10px 7px 8px rgba(0, 0, 0, 0.5)); 
}

nav ul li a {
  text-decoration: none;
  font-size: 18px;
  color: black;
  cursor: pointer;
}

.logo {
  cursor: pointer;
  position: relative;
  width: 10%;
  top: 0.5%;
  left: 3%;
}

@media(max-width: 970px) {
  nav .menu-hamburguer {
    display: block;
  }

  nav ul {
    display: none;
  }
}
</style>