<script setup>
import { RouterLink } from 'vue-router'
import Contact from '../components/Contact.vue'
</script>

<template>
  <main id="about">
    <h1 class="name">I'm Archawit Changtor</h1>
    <p>
      Hi there! I'm a fourth year student living in Pathumthani, Thailand, currently studying
      Computer Engineering at
      <a class="link" href="https://www.siit.tu.ac.th" target="_blank"
        >Sirindhorn International Institute of Technology (SIIT)</a
      >
      with a major in Cloud Computing and Cyber Security.
      <br />
      <br />
      My interests lie in web development, web design, and cyber security. I'm actively developing a
      plenty of web development projects to build strong foundations and solve my daily problems.
      <br />
      <br />
      I graduated from
      <a class="link" href="https://gifted.kmutt.ac.th" target="_blank"
        >Darunsikkhalai Science School</a
      >, where I received a full scholarship from
      <a
        class="link"
        href="https://th.wikipedia.org/wiki/%E0%B9%82%E0%B8%84%E0%B8%A3%E0%B8%87%E0%B8%81%E0%B8%B2%E0%B8%A3%E0%B8%AA%E0%B8%99%E0%B8%B1%E0%B8%9A%E0%B8%AA%E0%B8%99%E0%B8%B8%E0%B8%99%E0%B8%81%E0%B8%B2%E0%B8%A3%E0%B8%88%E0%B8%B1%E0%B8%94%E0%B8%95%E0%B8%B1%E0%B9%89%E0%B8%87%E0%B8%AB%E0%B9%89%E0%B8%AD%E0%B8%87%E0%B9%80%E0%B8%A3%E0%B8%B5%E0%B8%A2%E0%B8%99%E0%B8%A7%E0%B8%B4%E0%B8%97%E0%B8%A2%E0%B8%B2%E0%B8%A8%E0%B8%B2%E0%B8%AA%E0%B8%95%E0%B8%A3%E0%B9%8C%E0%B9%83%E0%B8%99%E0%B9%82%E0%B8%A3%E0%B8%87%E0%B9%80%E0%B8%A3%E0%B8%B5%E0%B8%A2%E0%B8%99_%E0%B9%82%E0%B8%94%E0%B8%A2%E0%B8%81%E0%B8%B2%E0%B8%A3%E0%B8%81%E0%B8%B3%E0%B8%81%E0%B8%B1%E0%B8%9A%E0%B8%94%E0%B8%B9%E0%B9%81%E0%B8%A5%E0%B8%82%E0%B8%AD%E0%B8%87%E0%B8%A1%E0%B8%AB%E0%B8%B2%E0%B8%A7%E0%B8%B4%E0%B8%97%E0%B8%A2%E0%B8%B2%E0%B8%A5%E0%B8%B1%E0%B8%A2"
        target="_blank"
        >SCiUS</a
      >, and also participated in the
      <a class="link" href="https://www.facebook.com/sscomposn/" target="_blank"
        >Computer Olympic POSN Camp 1 and 2</a
      >
      during my school years. Currently, I'm receiving a four-year continuing scholarship from SIIT.
      <br />
      <br />
      For more information about my projects, feel free to check them out at
      <router-link class="link" to="projects">Projects</router-link>.
    </p>
  </main>
  <Contact></Contact>
</template>

<style scoped>
#about {
  display: flex;
  align-items: start;
  flex-direction: column;
}

#about h1 {
  margin-bottom: 1.1rem;
}

.profile-image {
  width: 8rem;
  height: 8rem;
  border-radius: 9999px;
  border: 3px solid var(--color-border);
  margin-top: 0.25rem;
  margin-bottom: 1.5rem;
}

@media only screen and (min-width: 600px) {
  .profile-image {
    display: block;
    width: 9rem;
    height: 9rem;
  }
}
</style>
