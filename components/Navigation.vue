<template>
  <nav class="nav">
    <ul>
      <li><NuxtLink to="/">Home</NuxtLink></li>
      <li><NuxtLink to="/about">About</NuxtLink></li>
      <li><NuxtLink to="/contact">Contact</NuxtLink></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Navigation',
}
</script>

<style scoped>
.nav {
  background-color: #000;
  padding: 10px;
}

.nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  margin: 0;
  padding: 0;
}

.nav li {
  margin: 0 15px;
}

.nav a {
  color: #fff;
  text-decoration: none;
}

.nav a:hover {
  text-decoration: underline;
}
</style>
