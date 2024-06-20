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
        <img @click="OpenMenu" src="../assets/menu-hamburguer.svg" class="menu-hamburguer">
    </nav>
</template>

<script>

export default {
methods: {
    OpenMenu() {
            this.$emit('OpenMenu');
        }
},
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
    position: relative;
    right: 5%;
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

.logo{
    position: relative;
    height: 8%;
    width: 80%;
    top: 0.5%;
    left: 2%;
}

@media(max-width: 970px){
    nav .menu-hamburguer{
        display: block;
        
    }
    nav ul{
        display: none;
    }
    /* nav ul{
        position: fixed;
        width: 60%;
        height: 60%;
        top: 0;
        left: 0;
        transform: translateX(-100%);
        display: flex;
        align-items: center;
        flex-direction: column;
        transition: 0.3s ease-in;
        background-color: #00000052;
    }
    nav ul.active{
        transform: translateX(0);

    }
    nav ul li{
        padding: 10px;
    }
    nav ul li a{
        font-size: 18px;
        color: white;
    }
     */
}
</style>