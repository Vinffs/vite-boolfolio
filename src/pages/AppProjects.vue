<template>
  <main class="container">
    <h1>This is the App Projects Component</h1>
    <div class="row">
      <div class="col-12 col-md-4 col-lg-3" v-for="project in store.projects" :key="project.id">

        <ProjectCard :project="project" />
      </div>
    </div>
  </main>
</template>

<script>
import axios from 'axios';
import { store } from '../assets/data/store.js';
import ProjectCard from "../components/ProjectCard.vue";
export default {
  name: 'AppProjects',
  components: {
    ProjectCard,
  },
  data() {
    return {
      store,
    }
  },
  methods: {
    getAllProjects() {
      axios.get(this.store.apiUrl + 'projects').then((response) => {
        this.store.projects = response.data.results.data;
      })
    }
  },
  mounted() {
    this.getAllProjects();
  }
}
</script>

<style lang="scss" scoped></style>