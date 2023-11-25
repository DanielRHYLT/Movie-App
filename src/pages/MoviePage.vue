<template>
  - <div class="movie-page">
      <div class="movie-list q-mr-md">
          <MovieList />
      </div>
  </div>
</template>

<style>

.movie-page {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 0 auto;
  width: 80%;
  padding: 20px;
  background-color: #f2f2f2;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
}

.movie-filter {
  width: 100%;
  margin-bottom: 20px;
}

.movie-list {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.movie-item {
  width: 200px;
  margin: 10px;
  background-color: #fff;
  padding: 20px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
}

.movie-item img {
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.movie-item h3 {
  font-size: 16px;
  font-weight: bold;
  margin-bottom: 10px;
}

.movie-item p {
  font-size: 14px;
  line-height: 1.5;
}
</style>

<script>

import MovieList from "../components/movies/movieList.vue";

export default {
  name: "MoviePage",
  components: {
      MovieList
  }
}

</script>
