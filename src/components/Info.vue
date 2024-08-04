<script>
export default {
  name: 'InfoComponent',

  data() {
    return {
      is_working: true,
      show_email: true,
      btnText: 'Hide Email',
      info: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequatur reprehenderit architecto possimus incidunt dolor molestias doloribus autem maxime dolorum dolore earum culpa, nobis ipsum eaque velit animi ullam voluptatibus asperiores!',
      backend_tecnologies: [
        { id: 0, label: 'JS' },
        { id: 1, label: 'PHP' },
        { id: 2, label: 'Python' }
      ],
      frontend_tecnologies: [
        { id: 0, label: 'JS' },
        { id: 1, label: 'CSS' },
        { id: 2, label: 'HTML' }
      ]
    }
  },

  methods: {
    toggleEmail() {
      this.show_email = !this.show_email
      if (this.show_email) {
        this.btnText = 'Show Email'
      } else {
        this.btnText = 'Hide Email'
      }
    }
  },

  props: {
    email: String
  }
}
</script>

<template>
  <div>
    <h3>Infos:</h3>
    <p>Email by prop: {{ email }}</p>
    <br />
    <p v-if="is_working">I'm working at this moment</p>
    <p v-else>I'm open to work.</p>
    <p>I'm working with these technologies:</p>
    <ul>
      <li v-for="tech in backend_tecnologies" v-bind:key="tech.id">{{ tech.label }}</li>
    </ul>
    <ul>
      <li v-for="tech in frontend_tecnologies" v-bind:key="tech.id">{{ tech.label }}</li>
    </ul>
    <div>
      <button @click="toggleEmail">{{ btnText }}</button>
    </div>
    <p v-show="show_email">Mande um e-mail para: {{ email }}</p>
    <p>
      para acessar meu portifílio clique <a v-bind:href="personal_link" target="_blank">aqui</a>
    </p>
  </div>
</template>
