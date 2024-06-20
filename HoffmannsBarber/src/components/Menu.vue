<template>
    <div class="container" v-if="ShowMenu">
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">Catálogo</a></li>
            <li><a href="#">Planos</a></li>
            <li><a href="#">Contato</a></li>
        </ul>
        <a href="home">
            <img class="logo1" src="../assets/logo-blank.svg">
        </a>
    </div>
</template>

<script>
export default {
    props: {
        ShowMenu: {
            type: Boolean,
            required: true
        },
    },
}
</script>

<style>
.container {
    background-color: #002445;
    display: flex;
    flex-direction: column;
    position: fixed;
    width: 30%;
    height: 100%;
    top: 0;
    left: 0;
    align-items: center;
    justify-content: center;
    transition: 0.3s ease-in;
    justify-content: space-between;
}

.container ul {
    display: flex;
    list-style: none;
    align-items: center;
    flex-direction: column;
    gap: 50px;
    position: relative;
    left: -10%;
    top: 30%;
}


.container ul li a {
    text-decoration: none;
    font-size: 18px;
    color: black;
    font-weight: 600;
}

.container ul li a:hover {
    color: white;

}

.container ul li {
    transition: 0.3s;
}

.container ul li:hover {
    transform: scale(1.1);
}

.logo1 {
    position: relative;
    height: 80%;
    width: 100%;
    top: 0.5%;
    left: 2%;
    filter: drop-shadow(1px 1px 4px white);

}
</style>