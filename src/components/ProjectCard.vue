<template>
  <div>
    <div class="card">
      <img :src="`${store.imgPath}${project.thumb}`" :alt="project.title">
      <router-link :to="{ name: 'single-project', params: { slug: project.slug } }" class="btn btn-primary">{{
        project.title
      }}</router-link>
    </div>

  </div>
</template>

<script>
import { store } from '../assets/data/store.js';
export default {
  name: 'ProjectCard',
  props: ['project'],
  data() {
    return {
      store,
    }
  }
}
</script>

<style lang="scss" scoped></style>