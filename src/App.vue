<template>
  <AppHeader></AppHeader>
  <router-view :key="$route.path"></router-view>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
export default {
  name: 'App',
  components: {
    AppHeader,
  },
  data() {
    return {

    }
  },
}
</script>

<style lang="scss" scoped>
@use "./assets/styles/partials/variables" as *;
</style>