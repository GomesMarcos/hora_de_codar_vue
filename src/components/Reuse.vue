<script>
export default {
  name: 'ReuseComponent',
  data() {
    return {
      is_activate: false
    }
  },

  methods: {
    toggle_activate() {
      return (this.is_activate = !this.is_activate)
    }
  }
}
</script>

<style scoped>
div {
  margin-bottom: 2em;
}
</style>

<template>
  <div>
    <button @click="toggle_activate">Toggle activation</button>
    <span v-show="is_activate">Is active!</span>
  </div>
</template>
