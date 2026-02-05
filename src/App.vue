<template>
  <div 
    v-for="(obj, index) in todos" 
    v-bind:key="obj.id"
    class="todos-item"
  > 
    <!-- : ou v-bind = uma instrução para dizer que esse atributo vai ser um atributo dinâmico. -->
    <img :src="obj.imgUrl" v-if="obj.imgUrl" :alt="imgAlt">
    {{ index + 1 }} - {{ obj.title }}
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      imgAlt: 'Imagem de exemplo',
      todos: [
        {
          "userId": 1,
          "id": 1,
          "title": "delectus aut autem",
          "completed": false,
          "imgUrl": 'https://placehold.co/150x150',
          
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
