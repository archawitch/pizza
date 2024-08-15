<script>
import { RouterLink } from 'vue-router'
</script>

<template>
  <nav id="nav">
    <router-link to="/projects" active-class="active-nav">Projects</router-link>
    <router-link to="/" active-class="active-nav">About</router-link>
  </nav>
</template>

<style scoped>
nav {
  width: 100%;
  display: flex;
  align-items: baseline;
  justify-content: end;
  margin-bottom: 2rem;
}

nav a {
  margin-left: 1.5rem;
}

@media only screen and (min-width: 640px) {
  nav {
    margin-bottom: 2.75rem;
  }
}
</style>
