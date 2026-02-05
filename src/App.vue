<template>
  <div>
    One-way data binding <br>
    Two-Way data binding <br>
    v-model -> formulários

    <br><br>
    <label>Nome</label><br>
    <input 
      v-model="name"
      type="text"
    ><br>
    {{ name }}
    
    <br><br>

    <label>Sports</label><br>
    <select v-model='sports'>
      <option value="">Escolha</option>
      <option value="soccer">Futebol</option>
      <option value="basketball">basquete</option>
      <option value="tenis">Tênis</option>
    </select> <br>
    {{ sports }}

    <br><br>
    <label>Newsletter</label><br>
    <input 
      v-model="newsletter"
      type="radio"
      value="sim"
    /> Sim

    <input 
      v-model="newsletter"
      type="radio"
      value="nao"
    /> Não <br>

    {{ newsletter }}

    <br><br>

    <label>Contrato</label><br>
    <input
      v-model="contract"
      type="checkbox"
    /> Aceito os termos... <br>
    {{ contract }}

    <br><br>
    <label>Selecione as cores</label><br>
    <input
      v-model="colors" 
      type="checkbox"
      value="yellow"
    > Amarelo <br>

    <input
      v-model="colors" 
      type="checkbox"
      value="green"
    > Verde <br>

    <input
      v-model="colors" 
      type="checkbox"
      value="red"
    > Vermelho <br>

    {{ colors }}


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
