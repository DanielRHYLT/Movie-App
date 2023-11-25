<template>
  <div class="movie-card">
    <img v-bind:src="'http://image.tmdb.org/t/p/w500/' +  movie.poster_path" alt="Poster de la película">
    <h3>{{ movie.title }}</h3>
    <p>{{ movie.description }}</p>
    <div class="movie-info">
      <span class="genres">Géneros: {{ movie.genre_ids }}</span>
      <span class="rating">Calificación: {{ movie.vote_average }}</span>
      <span class="language">Lenguaje: {{ movie.original_language }}</span>
    </div>
    <q-btn @click="addToFavorites(movie)" color="primary" icon="star" label="Agregar a favoritos" />
  </div>
</template>

<style>
.movie-card {
  width: 300px;
  height: 400px;
  margin: 10px;
  border: 3px solid #1a0444;
  background-color: #ffffff;
}

.movie-card img {
  width: 100%;
  height: 200px;
}

.movie-card h3 {
  font-size: 18px;
  font-weight: bold;
  text-align: center;
  line-height: 1.5;
}

.movie-card p {
  font-size: 16px;
}

.movie-card .movie-info {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.movie-card .genres {
  font-size: 14px;
  color: #999;
}

.movie-card .rating {
  font-size: 20px;
  font-weight: bold;
  color: #f00;
}

.movie-card .language {
  font-size: 14px;
  color: #999;
}

.movie-card a {
  text-decoration: none;
  color: #f00;
}


</style>

<script>
export default {
  name: "MovieItem",
  props: {
    movie: {
      type: Object,
      required: true,
    },
  },
};
</script>
