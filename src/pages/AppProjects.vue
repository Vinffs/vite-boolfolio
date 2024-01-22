<template>
  <div>
    <h1>This is the App Projects Component</h1>
    <li v-for="project in store.projects">
      <router-link :to="{ name: 'single-project', params: { slug: project.slug } }" class="btn btn-primary">{{
        project.title
      }}</router-link>
    </li>
  </div>
</template>

<script>
import axios from 'axios';
import { store } from '../assets/data/store.js';
export default {
  name: 'AppProjects',
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