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
        <li class="project-item" name="iwin">
          <router-link class="link" to="/project/iwin">iWin</router-link>&nbsp;- Go, Swift
          <span class="project-date text-secondary">Aug 24</span>
        </li>
        <li class="project-item" name="tasky">
          <router-link class="link" to="/project/tasky">Tasky</router-link>&nbsp;- ReactJS
          <span class="project-date text-secondary">Jul 24</span>
        </li>
      </ul>
    </section>
    <section name="projects-2023">
      <h2>2023</h2>
      <ul class="project-list">
        <li class="project-item" name="picterest">
          <router-link class="link" to="/project/picterest">Picterest</router-link>&nbsp;- VueJS,
          PHP, MySQL
          <span class="project-date text-secondary">Nov 23</span>
        </li>
      </ul>
    </section>
    <section name="projects-2022">
      <h2>2022</h2>
      <ul class="project-list">
        <li class="project-item" name="catch-the-fruit">
          <router-link class="link" to="/project/catch-the-fruits">Catch the fruits</router-link>
          &nbsp;- Java
          <span class="project-date text-secondary">Apr 22</span>
        </li>
      </ul>
    </section>
  </main>
  <Contact></Contact>
</template>

<style scope>
.project-list {
  margin-top: 0.85rem;
  padding-left: 0;
}

.project-item {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 0.5rem;
}

.project-date {
  margin-left: auto;
}
</style>
