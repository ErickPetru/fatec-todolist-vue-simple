<template>
  <form @submit.prevent="insert">
    <input v-model="text" :placeholder="placeholder">
    <button>Inserir</button>
  </form>
</template>

<script>
export default {
  props: {
    placeholder: String
  },

  data () {
    return {
      text: ''
    }
  },

  methods: {
    insert () {
      this.$emit('inserted', this.text)
      this.text = ''
    }
  }
}
</script>

<style scoped>
input {
  font: 1em Sans-serif;
  padding: 1em;
  background: #fff;
  border: 1px solid #999;
}

button {
  font: 1em Sans-serif;
  padding: 1em;
}
</style>
