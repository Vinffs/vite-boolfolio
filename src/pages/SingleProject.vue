<template>
  <div>
    <h1>{{ project.title }}</h1>
    <img :src="`${store.imgPath}${project.thumb}`" :alt="project.title">
    <div>
      <router-link :to="{ name: 'single-project', params: { slug: 'htmlcss-discord' } }">vedi altro
        progetto</router-link>
    </div>
  </div>
</template>

<script>
import axios from 'axios';
import { store } from '../assets/data/store.js';
export default {
  name: 'SingleProject',
  data() {
    return {
      store,
      project: "",
    }
  },
  methods: {
    getProjectData() {
      axios.get(this.store.apiUrl + "projects/" + this.$route.params.slug).then((res) => {
        this.project = res.data.results;
      })
    }
  },
  mounted() {
    this.getProjectData();
  }
}
</script>

<style lang="scss" scoped></style>