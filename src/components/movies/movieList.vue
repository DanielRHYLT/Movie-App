<template>
  <h5>Listado de Peliculas</h5>
  <div class="movie-list">
      <div class="movie-grid">
          <div class="movie-item" v-for="pelicula in movies" :key="pelicula.id">
              <MovieItem :movie="pelicula" />
          </div>
      </div>
  </div>
</template>

<style>
.movie-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 30px;
}
</style>

<script>
import axios from "axios";
import MovieItem from "./MovieItem.vue";

export default {
  name: "MovieList",
  components: {
    MovieItem,
  },
  data() {
    return {
      movies: [],
    };
  },
  mounted() {
    this.getMovies()
  },
  methods: {
    getMovies() {
      var url = 'https://api.themoviedb.org/3/discover/movie'
      var cabeceraToken = {
          headers: {
              accept: 'application/json',
              Authorization: 'Bearer eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiJlMGNkYmU3ZWY4NzJjNTAwMTA4MjlmYmQ2MWRiM2I4NiIsInN1YiI6IjY1NjBmMDA2YTZjMTA0MDBlMTY0YTllYiIsInNjb3BlcyI6WyJhcGlfcmVhZCJdLCJ2ZXJzaW9uIjoxfQ.IBHcPO66VhFi9Qa1XxSnRLJycA1VXPQtjFgO_XfjZOk'
          }
      }
      axios.get(url, cabeceraToken).then(response => {
        console.log('API Response:', response.data);
        this.movies = response.data.results
        console.log("Movies: ",this.movies)
      }).catch(error => {
        console.log("Error: " + error)
      })
    }
  }
};
</script>
