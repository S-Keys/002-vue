<template>
    <h1>Eu sou o componente {{ nome }}</h1>
</template>

<script>
    export default {
        name: 'LifeCycle',
        data() {
            return {
                nome: 'LifeCycle'
            }
        },
        created() {
            setTimeout(() => {
                this.nome = 'LifeCycle + 2s'
            }, 2000);
        },
        mounted() {
            setTimeout(() => {
            this.nome = 'LifeCycle + 4s'
        }, 4000);
    }
    }
</script>