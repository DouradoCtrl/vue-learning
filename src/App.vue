<template>
  <div>
    {{ fullName }}
    <h1>Todos em aberto</h1>
    <div
      v-for="todo in uncompletedTodos"
      :key="todo.id"
    >
      {{ todo.title }} <!-- <span>{{ todo.completed }}</span> -->
    </div>

    <h1>Todos completas</h1>
    <div
      v-for="todo in completedTodos"
      :key=todo.id
    >
      {{ todo.title }} <!-- <span>{{ todo.completed }}</span> -->
    </div>

    <h1>Todos</h1>
    <div 
      v-for="todo in todos"
      :key=todo.id
    >
      <input
        v-model="todo.completed" 
        type="checkbox"
      >
      {{ todo.title }} <!-- <span>{{ todo.completed }}</span> -->
    </div>
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
      },
      todos: [
      {
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
  },

  computed: {
    fullName() {
      return `${this.user.first_name} ${this.user.last_name}`
    },
    completedTodos() {
      return this.todos.filter(todo => todo.completed );
    },
    uncompletedTodos() {
      return this.todos.filter(todo => !todo.completed);
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

span {
  font-weight: bold;
}
</style>
