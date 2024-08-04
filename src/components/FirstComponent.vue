<script>
import MultipleEvents from './MultipleEvents.vue'
import Reuse from './Reuse.vue'

export default {
  name: 'FirstComponent',
  data() {
    return {
      name: 'Marcos',
      job: 'Dev'
    }
  },

  components: {
    MultipleEvents,
    Reuse
  },

  created() {
    setTimeout(() => {
      this.name = 'Eqeqwepokw'
    }, 1000)
  },
  mounted() {
    setTimeout(() => {
      this.name = 'fnwefgn'
    }, 2000)
  }
}
</script>

<template>
  <div>
    <p>Meu nome é: {{ name }}</p>
    <p>Profissão: {{ job }}</p>
    <MultipleEvents />
    <Reuse />
    <Reuse />
    <Reuse />
  </div>
</template>
