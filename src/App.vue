<template>
  <div>
    {{ fullName }}
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      user: {
        first_name: "Samuel",
        last_name: "Dourado"
      }
    }
  },

  computed: {
    fullName() {
      return `${this.user.first_name} ${this.user.last_name}`
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
