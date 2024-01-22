<template>
  <HeaderComponent />
</template>

<script>
import HeaderComponent from "./components/HeaderComponent.vue";
export default {
  name: 'App',
  components: {
    HeaderComponent,
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