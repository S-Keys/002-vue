<template>
    <div>
        <div>
            <p v-if="esta_trabalhando">Atualmente empregado</p>
            <p v-else="esta_trabalhando">No momento estou estudando, já que estou desempregado. Em caso de oportunidades para Dev Jr, envie um mensagem no e-mail abaixo</p>
        </div>
        <div>
            <Picture/>        
        </div>
        <div>
            <div>
                <button @click="showEmail">{{ textoBotao }}</button>
                <p v-show="mostrar_email"> Testando V-SHOW (como true) como ferramenta para Mostrar o e-mail: <b class="destaque">{{ email }}</b></p>
            </div>
            <p>Utilizo as seguintes tecnologias para frontend:</p>
            <ul>
                <li v-for="(tecnologias, index) in frontend_tecnologias" v-bind:key="index">
                    {{ tecnologias }}
                </li>
            </ul>
        </div>
        <div>
            <p>Pretendo utilizar as seguintes tecnologias para backend:</p>
            <ul>
                <li v-for="tecnologias in backend_tecnologias" :key="tecnologias.id">
                    {{ tecnologias.language }}
                </li>
            </ul>
        </div>
        <div>
            <p>Para acessar meu portifólio basta <a v-bind:href="meu_link" target="_blank">clicar aqui</a></p>
            <p v-if="4 > 2">Testando V-IF em um parágrafo</p>
        </div>
    </div>
</template>

<script>
import Picture from './Picture.vue'

    export default {
        name: 'Info',
        components: {
            Picture
        },
        props: {
          email: String,
          esta_trabalhando: Boolean
        },
        data(){
            return{
                //esta_trabalhando: false,
                mostrar_email: false,
                meu_link: 'https://007-sergio-chaves-portifolio-9fs1cr3je-s-keys.vercel.app/curriculo.html',
                textoBotao: 'Exibir meu e-mail',
                frontend_tecnologias: ['HTML 5... Nada demais','CCS 3... já é alguma coisa','JavaScriptaqui começa a ficar interessante','Vue... Já dá para trabalhar!'],
                backend_tecnologias: [
                    {id: 1, language: 'PHP'},
                    {id: 2, language: 'Python'},
                    {id: 3, language: 'React'}
                ]
            } 
        },
        methods: {
            showEmail() {
                this.mostrar_email = !this.mostrar_email
                if(!this.mostrar_email) {
                    this.textoBotao = 'Exibir meu e-mail'
                } else {
                    this.textoBotao = 'Ocultar meu e-mail'
                }
        }
    }
}
</script>