<template>
    <div class="container">
        <div class="row" v-if="movies.length > 0">
        <movie :movie="movie" v-for="movie in movies" :key="movie.id"></movie>
    </div>
    <div v-else  class="alert alert-danger">
        Sorry, we couldn`t find value for your search, please, try again.
    </div>
    </div>
</template>

<script>
import Movie from './MovieItem';
import { mapGetters } from 'vuex';

export default {
  components: {
    Movie
  },
  computed: {
    ...mapGetters({
      movies: 'filteredMovies',
    })
  }
};
</script>

<style scoped>
</style>