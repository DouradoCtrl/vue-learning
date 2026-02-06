<template>
  <div>
    <TheHeader v-if="showHeader"/>
    <button
      @click="activeAndDesactiveHeader()"
    >
      Ativar e Desativar
    </button>

    <div>
    </div>
    <h1>Hello Word</h1>
    <input type="text" v-model="name">
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
      showHeader: true,
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
  },

  updated() {
    console.log('updated', this.name);
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
    activeAndDesactiveHeader() {
      this.showHeader = !this.showHeader;
    },
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
