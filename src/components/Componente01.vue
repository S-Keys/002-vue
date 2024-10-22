<template>
    <div>
        <h1>Éeeeeee Vue... vamos lá também!</h1>
        <p>Meu nome é {{ nome }} e minha profissão é {{ profissao }}</p>
        <MultiplosEventos/>
        <Reutilizacao/>
        <Reutilizacao/>
        <Reutilizacao/>
    </div>
</template>
<script>
    import MultiplosEventos from './MultiplosEventos.vue';
    import Reutilizacao from './Reutilizacao.vue'

    export default {
        name: 'Componente_01',
        components: {
            MultiplosEventos,
            Reutilizacao
        },
        data() {
            return {
                nome: "Sérgio",
                profissao: "Futuro Dev Jr"
            }
        }
    }
</script>