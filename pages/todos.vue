<template>
  <div>
    <ul>
      <li v-for="todo in todos">
        <input type="checkbox" :checked="todo.done" id="" @change="toggle(todo)">
        <span :class="{ done: todo.done}">{{ todo.text }}</span>
      </li>
    </ul>
    <input placeholder="タスク追加" @keyup.enter="addTodo">
  </div>
</template>

<script>
import { mapMutations } from 'vuex'

export default {
  computed: {
    todos(){
      return this.$store.state.todos.list
    }
  },
  methods: {
    addTodo(e){
      this.$store.commit('todos/add', e.target.value)
    },
    ...mapMutations({
      toggle: 'todos/toggle'
    })
  }
}
</script>