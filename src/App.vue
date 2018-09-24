<template>
  <div id="app" class="container text-center">
    <movies-app></movies-app>
  </div>
</template>

<script>
import MoviesApp from "./components/MoviesApp.vue";
export default {
  name: "app",
  components: {
    MoviesApp
  }
};
</script>