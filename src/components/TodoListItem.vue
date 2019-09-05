<template>
  <li><b>{{ item.id }}</b> - {{ item.text }}</li>
</template>

<script>
export default {
  props: {
    item: Object
  }
}
</script>

<style scoped>
li {
  padding: 1em;
  background: #ef7;
  border: 1px solid #0002;
}
</style>
