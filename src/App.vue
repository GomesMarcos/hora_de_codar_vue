<script>
import FirstComponent from './components/FirstComponent.vue'
import LifeCycle from './components/LifeCycle.vue'
import Person from './components/Person.vue'
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    FirstComponent,
    LifeCycle,
    Person,
    Header
  }
}
</script>

<template>
  <div>
    <Header></Header>
    <LifeCycle />
    <FirstComponent />
    <Person />
  </div>
</template>

<style>
body {
  background-color: #333;
  color: white;

  a {
    color: red;
  }
}
</style>
