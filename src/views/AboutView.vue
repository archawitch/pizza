<script setup>
import { RouterLink } from 'vue-router'
import Contact from '../components/Contact.vue'
</script>

<template>
  <main id="about">
    <h1>I'm Archawit Changtor</h1>
    <p>
      Hi there! I'm a fourth year student living in Pathumthani, Thailand, currently studying
      Computer Engineering at
      <a class="link" href="https://www.siit.tu.ac.th" target="_blank"
        >Sirindhorn International Institute of Technology (SIIT)</a
      >
      with a major in Cloud Computing and Cyber Security.
      <br />
      <br />
      My interests lie in web development, mobile app development, UI design, and cyber security.
      I'm actively developing a plenty of projects to build strong foundations and solve my daily
      problems.
      <br />
      <br />
      For more information about my personal projects, feel free to check them out at
      <router-link class="link" to="projects">Projects</router-link>.
    </p>
  </main>
  <Contact></Contact>
</template>

<style scoped>
#about {
  display: flex;
  align-items: center;
  flex-direction: column;
}

#about h1 {
  margin-bottom: 1.1rem;
  width: 100%;
}
</style>
