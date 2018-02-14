<script>
import Search from "./search";
import List from "./list";

export default {
  components: {
    Search,
    List
  },

  data () {
    return {
      moviesList: []
    }
  },

  /*created: function () {
    this.fetchData()
  },*/

  methods: {
    fetchData: function (query) {
      var apiUrl = 'http://www.omdbapi.com/?apikey=f1061c47&S='+query;
      this.$http.get(apiUrl).then(response => {
        this.moviesList = response.body.Search;
      });
    },
    doSearch: function (query) {
      this.fetchData(query);
    }
  }
}
</script>

<template>
  <div class="movies">
    <search @sm-search="doSearch" />
    <list :movies-list="moviesList" />
  </div>
</template>