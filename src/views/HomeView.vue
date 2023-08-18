<script>
import NewTodo from '@/components/Todo/NewTodo.vue'
import TodoList from '@/components/Todo/TodoList.vue'

export default {
  components: {
    NewTodo,
    TodoList
  },
  data: () => ({
    allTodos: [],
    todos: []
  }),
  computed: {
    // filteredTodos: () => {
    //   console.log('tiggereddddd')
    //   return this.allTodos?.filter((todo) => todo.userId === 1)
    // },
    // todos: () => {
    //   return this.filteredTodos
    // }
  },
  methods: {
    async fetchTodos() {
      console.log('I rannn')
      this.allTodos = await fetch('https://jsonplaceholder.typicode.com/todos').then((response) =>
        response.json()
      )
      console.log(this.allTodos, 'alltodo')
    }
  },
  watch: {
    allTodos(newValue) {
      this.todos = newValue.length > 0 && this.allTodos.filter((todo) => todo.userId === 1)
    }
  },
  created() {
    this.fetchTodos()
  }
}

// const res = await fetch('https://jsonplaceholder.typicode.com/todos')
// const allTodos = await res.json()
</script>

<template>
  <div class="list">
    <NewTodo />
    <TodoList :todos="todos" />
  </div>
</template>

<style scoped>
.list {
  background-color: #f3deba;
  border-radius: 3rem;
  padding: 2rem 1rem;
}

@media (min-width: 1024px) {
  .list {
    padding: 2rem;
  }
}
</style>
