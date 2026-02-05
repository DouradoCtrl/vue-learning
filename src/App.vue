<template>
  <div>
    <!-- Sintaxe antiga (return undefined)-->
    <button
      type="submit"
      v-on:click="onClick()" 
    >
      Enviar
    </button>  

    <br><br>
    <!-- Sintaxe nova -->
    <!--  Utilizei evento modificadores:
      - once
    -->
    <button
      type="submit"
      @click.once="onClick"
    >
      Enviar
    </button>  

    <br><br>
    <!-- Event Over and Out -->
    <div
      @mouseover="onMouseOver"
      @mouseout="onMouseOut"
    >
      Ao passar do mouse
    </div>
    
    <br><br>
    <!-- Form actions -->
    <!-- Utilizado modificadores de evento
      - prevent
      - enter
    -->

    <form 
      action="https://www.google.com"
      @submit.prevent="onSubmit"
    >
      <input 
        type="text"
        @keyup.enter="onKeyUp"
      >
      <button type="submit"
      >
        Submit
      </button>
    </form>

  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      name: 'Pedro',
      sports: '',
      newsletter: 'sim',
      contract: true,
      colors: [],

    }
  },

  methods: {
    onClick($evt) {
      console.log("Enviado:", $evt)
    },
    onMouseOver($evt) {
      console.log("Mouse Over:", $evt)
    },
    onMouseOut($evt) {
      console.log("Mouse Out:", $evt)
    },
    onSubmit($evt) {
      console.log("Submit:", $evt)
    },
    onKeyUp($evt) {
      console.log("Key Up:", $evt)
    }
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
