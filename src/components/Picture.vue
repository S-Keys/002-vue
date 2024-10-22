<template>
    <div>
        <MudarImagem @troca-imagem="trocaImagem"/>
        <img :src="avatar" :alt="descricao">
    </div>
</template>

<script>
    import Reutilizacao from './Reutilizacao.vue'
    import MudarImagem from './MudarImagem.vue';

    export default {
        name: 'Picture',
        components: {
            Reutilizacao,
            MudarImagem
        },
        data() {
            return {
                avatar: "./Img/Untitled.jpg",
                descricao: "Gato digitando em um notebook"
            }
        },
        methods: {
            trocaImagem() {
                this.avatar = "./Img/Batman & Robin.gif"
            }
        }
    }
</script>