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
  width: 350px;
  height: 450px;
  margin: 10px;
  background-color: #e7d4d4;
  padding: 20px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
  align-items: center;
  justify-content: center;
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
.movie-page {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 0 auto;
  width: 100%;
  padding: 20px;
  background-color: rgb(33, 4, 80);
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
  align-items: center;
  justify-content: center;
}
h5 {
  font-size: 30px;
  font-weight: bold;
  margin-bottom: 20px;
  color: #fff;
}
.q-btn:before {
  background-color: blue;
  align-items: center;
  justify-content: center;
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
