<template>
  <div>
    <h1>Hello Word</h1>
    {{ name }}
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      name: 'Steve Jones'
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

  beforeUnmount() {
    console.log('beforeUnmount');
    console.log('Estado:', this.name);
    console.log('DOM', this.$el);
  },

  unmounted() {
    console.log('unmounted');
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
