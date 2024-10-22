<template>
  <div>
    <Header v-bind:esta_logado="true"/>
    <Componente01/>
    <LifeCycle/>
    <p>Esta informação é um {{ testando }}</p>
    <Pessoa/>
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Componente01 from './components/Componente01.vue' 
import HelloWorld from './components/HelloWorld.vue'
import LifeCycle from './components/LifeCycle.vue'
import Pessoa from './components/Pessoa.vue';

export default {
  name: 'App',
  components: {
    Header,
    HelloWorld,
    Componente01,
    LifeCycle,
    Pessoa
  },
    data(){
      return{
        testando: 'Teste no componente Root (que também é um componente)'
      }
    }
}
</script>

<style>
/*Estilização global*/
#app {
  background:rgb(27, 26, 26);
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color:rgb(163, 141, 99);
  
}

/*Estilização de artributo*/
a {
  color: orange;
}

/*Estilização em uma classe*/
.destaque{
  color: orange;
}

img {
  scale: 80%;
}

</style>
