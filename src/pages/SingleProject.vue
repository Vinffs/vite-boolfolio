<template>
  <div>
    This is the Single Post
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
    }
  },
  methods: {
    getProjectData() {
      // axios.get(`${this.store.apiUrl}projects/${this.$route.params.slug}`).then((response) => {
      //   console.log(response);
      // });
    }
  },
  mounted() {
    this.getProjectData();
  }
}
</script>

<style lang="scss" scoped></style>