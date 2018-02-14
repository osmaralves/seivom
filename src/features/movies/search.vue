<script>
export default {
  data () {
    return {
      query: ""
    }
  },

  methods: {
    doQuery: function () {
      this.$emit('sm-search', this.query);
    }
  }
}
</script>

<template>
  <form class="form-inline" v-on:submit.prevent="doQuery">
    <div class="form-group">
    	<input class="form-control" type="text" v-model="query">
    </div>
    <button class="btn btn-primary">»</button>
  </form>
</template>

