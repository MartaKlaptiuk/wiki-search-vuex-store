<template>
  <div class="results">
    <div class="item" v-for="item in results" :key="item">
      <a :href="item.url">{{ item.title }}</a>
      <div class="url">{{ item.url }}</div>
      <div v-html="item.snippet"></div>
    </div>
  </div>
</template>

<script>
export default {
  computed: {
    results() {
      return this.$store.getters.results;
    }
  }
};
</script>

<style>
.results {
  padding: 20px;
}

.item {
  margin-bottom: 25px;
}

.item a {
  text-decoration: none;
}

.url {
  color: green;
}
</style>
