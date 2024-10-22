<template>
    <div>
        <h2>Esta é a descrição da pessoa: <b class="destaque">{{ nome }}</b></h2>
        <Info :email="email" :esta_trabalhando="false"/>
        <Form/>
    </div>
</template>
<script>
    import Info from './Info.vue'
    import Form from './Form.vue'

    export default {
        name: 'Pessoa',
        components: {
            Info,
            Form
        },
        data() {
            return {
                nome: 'Sérgio Chaves',
                email: 'sergio.chaves@outlook.com'
            }
        }
    }
</script>