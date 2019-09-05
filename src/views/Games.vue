<template>
  <div id="games">
    <h1>Games</h1>
    <insert-box @inserted="add" placeholder="Qual o nome do game?" />
    <todo-list :items="games" />
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
      games: []
    }
  },

  methods: {
    add (text) {
      this.games.push({
        id: this.games.length + 1,
        text: text
      })
    }
  }
}
</script>
