<template>
  <p>{{ greeting }}</p>
  <input v-if="isVisible" type="text" v-model="greeting" />
  <button @click="toggleInput">Toggle Input</button>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data: () => {
    return {
      greeting: 'Hello World!',
      isVisible: false
    }
  },
  methods: {
    toggleInput() {
      this.isVisible = !this.isVisible
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
[v-cloak] {
  display: none;
}
</style>
