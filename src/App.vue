<template>
  <BaseAlert 
    :variant="info" 
  >
  {{ text }}
  </BaseAlert>
  
</template>

<script>
import BaseAlert from '@/components/BaseAlert.vue';


export default {
  name: 'App',
  components: { BaseAlert },
  data() {
    return {
      info: 'success',
      text: 'Formulário enviado com sucesso'
    }
  },

  beforeUpdate() {},
  updated() {},
  beforeCreate() {},
  created() {},
  beforeMount() {},
  mounted() {},

  watch: {
  },
  
  computed: {
  },
  
  methods: {
  },
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
