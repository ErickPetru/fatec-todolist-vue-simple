<template>
  <div id="home">
    <h1>Tarefas</h1>
    <insert-box @inserted="add" placeholder="O que precisa ser feito?" />
    <todo-list :items="tasks" />
  </div>
</template>

<script>
import InsertBox from '../components/InsertBox'
import TodoList from '../components/TodoList'

export default {
  components: {
    InsertBox,
    TodoList
  },

  data () {
    return {
      tasks: []
    }
  },

  methods: {
    add (text) {
      this.tasks.push({
        id: this.tasks.length + 1,
        text: text
      })
    }
  }
}
</script>
