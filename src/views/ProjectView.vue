<script setup>
import data from '../assets/project-details/project-details.json'
import { useRoute, RouterLink } from 'vue-router'
import { ref, watch, onMounted, watchEffect } from 'vue'

const route = useRoute()

const projectData = ref({ name: '', covers: '', description: '' })

const getDetails = (projectName) => {
  const result = data.projects.filter(
    (project) => project.route.toLowerCase() === projectName.toLowerCase()
  )

  if (result && result.length > 0) {
    projectData.value = {
      ...result[0]
    }
  }
}

watch(projectData, (newData) => {
  if (newData) {
  }
})

onMounted(() => {
  const projectName = route.params.name
  if (projectName) {
    getDetails(projectName)
  }
})
</script>

<template>
  <main class="project">
    <div class="project-name" name="project-name">
      <h1>{{ projectData.name }}</h1>
      <router-link class="link" to="/projects">back</router-link>
    </div>
    <div class="project-cover">
      <img v-for="cover in projectData.covers" :key="cover" :src="`/images/projects/${cover}`" />
    </div>
    <section name="project-description">
      <p v-html="projectData.description"></p>
    </section>
  </main>
</template>

<style scoped>
.project {
  margin-bottom: 3rem;
}

.project-name {
  display: flex;
  align-items: baseline;
  justify-content: space-between;
  flex-wrap: wrap;
  margin-bottom: 0.5rem;
}

.project-name-paragraph {
  font-weight: 500;
}

.project-cover {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
}

.project-cover:has(img:nth-child(2)) {
  justify-content: space-between;
}

.project-cover:has(img:nth-child(2)) img {
  width: 48%;
}

.project-cover:not(:has(img:nth-child(2))) img {
  width: 100%;
}
</style>
