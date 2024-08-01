<script setup>
import { RouterLink } from 'vue-router'
import Contact from '../components/Contact.vue'
</script>

<template>
  <main id="projects">
    <h1>Projects</h1>
    <section name="projects-2024">
      <h2>2024</h2>
      <ul class="project-list">
        <li class="project-item">
          <div name="tasky">
            <router-link class="link" to="/project/tasky">Tasky</router-link> - ReactJS
          </div>
          <span class="text-secondary">Jul 2024</span>
        </li>
      </ul>
    </section>
    <section name="projects-2023">
      <h2>2023</h2>
      <ul class="project-list">
        <li class="project-item">
          <div name="picterest">
            <router-link class="link" to="/project/picterest">Picterest</router-link> - VueJS, PHP,
            MySQL
          </div>
          <span class="text-secondary">Nov 2023</span>
        </li>
      </ul>
    </section>
    <section name="projects-2022">
      <h2>2022</h2>
      <ul class="project-list">
        <li class="project-item">
          <div name="catch-the-fruit">
            <router-link class="link" to="/project/catch-the-fruits">Catch the fruits</router-link>
            - Java
          </div>
          <span class="text-secondary">Apr 2022</span>
        </li>
      </ul>
    </section>
  </main>
  <Contact></Contact>
</template>

<style scope>
#projects {
  margin-bottom: 4.75rem;
}

.project-list {
  margin-top: 0.85rem;
  padding-left: 0;
}

.project-item {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>
