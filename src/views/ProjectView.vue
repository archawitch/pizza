<script setup>
import data from '../assets/project-details/project-details.json'
import { useRoute, RouterLink } from 'vue-router'
import { ref, onMounted } from 'vue'

const route = useRoute()

const projectData = ref({ name: '', coverType: '', covers: '', description: '' })

const getDetails = (projectName) => {
  const result = data['projects'].filter(
    (project) => project['route'].toLowerCase() === projectName.toLowerCase()
  )

  if (result && result.length > 0) {
    projectData.value = {
      ...result[0]
    }
  }
}

onMounted(() => {
  const projectName = route.params.name
  if (projectName) {
    getDetails(projectName)
  }
})
</script>

<template>
  <main class="project">
    <div class="project-title" name="project-name">
      <h1>{{ projectData['name'] }}</h1>
      <router-link class="link" to="/projects">back</router-link>
    </div>
    <div v-if="projectData['cover-type'] === 'image'" class="project-cover">
      <img
        v-for="cover in projectData['covers']"
        class="project-cover-item"
        :key="cover"
        :src="`/images/projects/${cover}`"
      />
    </div>
    <div v-if="projectData['cover-type'] === 'video'" class="project-cover">
      <div class="project-cover-item">
        <iframe
          v-for="cover in projectData['covers']"
          class="yt-video"
          :key="cover"
          :src="cover"
          height="100%"
          allowfullscreen="true"
        />
      </div>
    </div>
    <section name="project-description">
      <p v-html="projectData['description']"></p>
    </section>
  </main>
</template>

<style scoped>
.project-title {
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

.project-cover:has(.project-cover-item:nth-child(2)) {
  justify-content: space-between;
}

.project-cover:has(.project-cover-item:nth-child(2)) > .project-cover-item {
  width: 48%;
}

.project-cover:not(:has(.project-cover-item:nth-child(2))) > .project-cover-item {
  width: 100%;
}

.project-cover-item:has(.yt-video) {
  position: relative;
  padding-bottom: 56.25%; /* 16:9 */
  height: 0;
}

.yt-video {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: none;
}
</style>
