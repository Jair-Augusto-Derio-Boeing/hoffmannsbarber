<template>
    <nav>
        <a href="home">
            <img class="logo" src="../assets/logo-blank.svg" >
        </a>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">Catálogo</a></li>
            <li><a href="#">Planos</a></li>
            <li><a href="#">Contato</a></li>
        </ul>
        <img src="../assets/menu-hamburguer.svg" class="menu-hamburguer">
    </nav>
</template>

<script>

export default {

}
</script>

<style>
nav {
    width: 100%;
    height: 12vh;
    background-color: #D9D9D9;
    position: sticky;
    top: 0px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.menu-hamburguer {
    cursor: pointer;
    display: none;
}
nav ul{
    display: flex;
    list-style: none;
    align-items: center;
}
nav ul li{
    padding: 0 40px 0 20px;
    
}
nav ul li a{
    text-decoration: none;
    font-size: 18px;
    color: black;
}

.logo {
    width: 8%;
    margin-top: 0.5%;
    margin-left: 1%;
}
</style>