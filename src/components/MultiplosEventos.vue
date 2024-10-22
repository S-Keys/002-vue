<template>
    <div>
        <button @click="primeiro(txt1, $event), segundo(txt2, $event)">Ativar multiplos eventos</button>
        <p>{{ multiplos_eventos }}</p>
    </div>
</template>

<script>
    export default {
        name: 'MultiplosEventos',
        data() {
            return {
                multiplos_eventos: "",
                txt1: "Primeiro evento ativados!",
                txt2: "Segundo evento ativado após 2s!"
            }
        },
        methods: {
            primeiro(txt,e) {
                this.multiplos_eventos = txt;
            },
            segundo(txt,e) {
                setTimeout(() => this.multiplos_eventos = txt, 2000)
            }
        }
    }
</script>

<style scoped>
    div {
        margin: 20px;
    }
</style>