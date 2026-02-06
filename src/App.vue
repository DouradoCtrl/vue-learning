<template>
  <div>
    <TheHeader/>
    <h1>Hello Word</h1>
    {{ name }}
  </div>
</template>

<script>
import TheHeader from '@/components/TheHeader.vue';


export default {
  name: 'App',
  components: { TheHeader },
  data() {
    return {
      name: 'Steve Jones',
    }
  },

  /* 
    -== Ciclo de vida ==-
    -= Criação =-
      - Preparar o componente
      - Ajax, incializar algumas variáveis
      - Não tem acesso ao template (DOM)
    -= Montagem =-
      - Inicializar uma lib externa (new Lib())
      - Precisa de acesso ao template (DOM)
      - Ter acesso ao template (DOM)
    -= Atualização =-
      - Debug
      - Update
    -= Desmontagem =-
      - Remove tudo o que for necessário
      - Para liberar memória

    
  */

  // -== HOOKS
  beforeCreate() {
    console.log('beforeCreate');
    console.log('Estado:', this.name);
    console.log('DOM', this.$el);
  },

  created() {
    console.log('created');
    console.log('Estado:', this.name);
    console.log('DOM', this.$el);
  },

  beforeUpdate() {
    console.log('beforeUpdate');
    console.log('Estado:', this.name);
    console.log('DOM', this.$elg);
  },

  updated() {
    console.log('updated');
    console.log('Estado:', this.name);
    console.log('DOM', this.$elg);
  },

  beforeMount() {
    console.log('beforeMount');
    console.log('Estado:', this.name);
    console.log('DOM', this.$el);
  },

  mounted() {
    console.log('mounted');
    console.log('Estado:', this.name);
    console.log('DOM', this.$el);
  },

  watch: {
  },
  
  computed: {
  },
  
  methods: {

  }
}
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 60px;
}
</style>
