<template>
  <div 
    v-for="(obj, index) in todos" 
    v-bind:key="obj.id"
    class="todos-item"
  > 
    <!-- obj seria o objeto numero 1 do array -->
    <!-- precisa passar uma key em sistema robusto -->
    {{ index + 1 }} - {{ obj.title }}
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      todos: [
        {
          "userId": 1,
          "id": 1,
          "title": "delectus aut autem",
          "completed": false
        },
        {
          "userId": 1,
          "id": 2,
          "title": "quis ut nam facilis et officia qui",
          "completed": false
        },
        {
          "userId": 1,
          "id": 3,
          "title": "fugiat veniam minus",
          "completed": false
        },
        {
          "userId": 1,
          "id": 4,
          "title": "et porro tempora",
          "completed": true
        },
        {
          "userId": 1,
          "id": 5,
          "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
          "completed": false
        }
      ]
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

.todos-item {
    background-color: #3d3d3d;
    color: #fff;
    padding: 10px;
    margin-bottom: 10px;
  }
</style>
