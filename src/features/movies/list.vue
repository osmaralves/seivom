<script>
export default {
  props: {
    moviesList: Array
  }
}
</script>

<template>
  <div class="movies-list list-group">
    <div class="movies-list-item list-group-item" v-for="movie in moviesList">
      <img class="" :src="movie.Poster" :alt="movie.Title" />

      <div class="">
        <h5 class="">{{ movie.Title }}</h5>
        <p class="">{{ movie.Year }}</p>
        <p class="">{{ movie.Type }}</p>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
  .movies-list-item {
    display: flex;
  }
  .movies-list-item:hover {
    background: #e8e8e8;
  }
  .movies-list-item img {
    margin-right: 20px;
    height: 200px;
  }
</style>