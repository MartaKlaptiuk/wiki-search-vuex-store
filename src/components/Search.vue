<template>
  <div class="search">
    <h1>
      <span>B</span>
      <span>o</span>
      <span>o</span>
      <span>b</span>
      <span>l</span>
      <span>e</span>
    </h1>
    <input class="search-input" v-model="query">
    <button @click="search()">Search</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      query: ""
    };
  },
  methods: {
    search() {
      this.$store.dispatch("search", this.query);
    }
  }
};
</script>

<style lang="scss" scoped>
.search {
  display: flex;
  align-items: center;
  background-color: #f8f8f8;
  padding: 0 10px;

  h1 {
    margin-right: 20px;
  }

  span {
    &:nth-child(1) {
      color: #4285f4;
    }

    &:nth-child(2) {
      color: #db4437;
    }

    &:nth-child(3) {
      color: #f4b400;
    }

    &:nth-child(4) {
      color: #4285f4;
    }

    &:nth-child(5) {
      color: #0f9d58;
    }

    &:nth-child(6) {
      color: #db4437;
    }
  }

  input {
    height: 20px;
    width: 300px;
    outline: none;
    padding: 0 10px;
  }

  button {
    background-color: #4285f4;
    border: none;
    color: #ffffff;
    padding: 4px 15px;
    border-radius: 0 5px 5px 0;
    cursor: pointer;
  }
}
</style>


