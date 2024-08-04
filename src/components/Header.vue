<script></script>

<template>
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">Projetos</a></li>
    <li><a href="#">Contatos</a></li>
  </ul>
</template>

<style scoped>
ul {
  list-style: none;
  display: flex;
  background-color: #555;
}
li {
  margin-right: 1em;
}

a {
  color: #ddd;
  text-decoration: none;
  transition: 0.5;
}

a:hover {
  color: turquoise;
  background-color: transparent;
}
</style>
