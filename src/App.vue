<template>
  <div>
    <label>Nome: </label>
    <input
      v-model="name"
      type="text"
    > {{ name }}

    <br><br>
    <label>Objeto Watch</label><br>

    <input
      v-model="user.first_name" 
      type="text"
    > <br>

    <input
      v-model="user.last_name" 
      type="text"
    > <br>

    {{ fullName }}
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      name: 'Samuel',
      user: {
        first_name: '',
        last_name: '',
      }
    }
  },

  watch: {
    name() {
      console.log("Nome alterado");
    },

    user: {
      handler() {
        console.log("Nome em objeto alterado");
      },

      deep: true
    }
  },
  
  computed: {
    fullName() {
      return `${this.user.first_name} ${this.user.last_name}`
    }
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

span {
  font-weight: bold;
}
</style>
