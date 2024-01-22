<template>
  <div>
    <h1>Hello World</h1>
    <div v-for="project in projects">
      {{ project.title }}
    </div>

  </div>
</template>

<script>
import axios from 'axios';
import { store } from '../assets/data/store';
export default {
  name: 'HeaderComponent',

  data() {
    return {
      store,
      projects: [],
    }
  },
  methods: {
    getAllProjects() {
      axios.get(this.store.apiUrl + '/projects').then((res) => {
        this.projects = res.data.results.data;
      });
    }
  },
  mounted() {
    this.getAllProjects();
  }
}
</script>

<style lang="scss" scoped></style>