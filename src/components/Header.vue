<template>
    <ul>
        <li><a href="https://www.linkedin.com/in/sergiorlchaves/" target="blank">HOME</a></li>
        <li><a href="https://github.com/S-Keys" target="blank">PROJETOS</a></li>
        <li><a href="https://wa.me/5521992669642" target="blank">CONTATO</a></li>
        <li v-if="esta_logado"><a href="https://images.pexels.com/photos/18654869/pexels-photo-18654869/free-photo-of-oculos-escuros-oculos-de-sol-camera-maquina.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" target="blank">MEU PERFIL</a></li>
    </ul>    
</template>

<script>
    export default {
        name: 'Header',
        props: ["esta_logado"]
    }
</script>


<style scoped>
/*Estilização de scoped (específico)*/
    ul {
        list-style: none;
        display: flex;
        background-color: orange;
    }

    li {
        margin-right: 10px;
        padding: 10px 5px 10px 5px;
    }

    a {
        color:rgb(27, 26, 26);
        text-decoration: none;
        transition: .3s;
    }

    a:hover {
        color: orangered;
    }

</style>