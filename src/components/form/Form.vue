<script>
import InputText from './InputText.vue'
import Submit from './Submit.vue'

export default {
  name: 'Form',
  components: {
    InputText,
    Submit
  },
  data() {
    return {
      name: '',
      email: ''
    }
  },
  methods: {
    sendForm(e) {
      e.preventDefault()
      const name = this.name
      const email = this.email

      // AJAX
    }
  }
}
</script>

<template>
  <form action="" @submit="sendForm($event)">
    <div>
      <InputText v-model="name" />
    </div>
    <div>
      <InputText v-model="email" />
    </div>
    <div>
      <Submit />
    </div>
  </form>
</template>
