<script>
export default {
  name: 'MultipleEvents',
  data() {
    return {
      multiple_events_0: '',
      multiple_events_1: 'multiple_events_1'
    }
  },

  methods: {
    firstEvent(e) {
      this.multiple_events_0 = 'multiple_events_0'
    },
    seccondEvent(e) {
      setTimeout(() => {
        this.multiple_events_0 = this.multiple_events_1
      }, 500)
    },
    thirdEvent(e) {
      setTimeout(() => {
        this.multiple_events_0 = ''
      }, 1000)
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
    <button @click="firstEvent($event), seccondEvent($event), thirdEvent($event)">
      Ativar múltiplos eventos
    </button>
    <p>{{ multiple_events_0 }}</p>
  </div>
</template>
