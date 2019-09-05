<template>
  <div>
    <ul v-if="items.length > 0">
      <todo-list-item v-for="item of items"
        :key="item.id" :item="item" />
    </ul>
    <p v-else>Nada foi cadastrado!</p>
  </div>
</template>

<script>
import TodoListItem from './TodoListItem'

export default {
  components: {
    TodoListItem
  },

  props: {
    items: Array
  }
}
</script>

<style scoped>
ul {
  margin: 1em 0 0 0;
  padding: 0;
  font: 1.25em Sans-serif;
  list-style: none;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: .5em;
}
</style>
