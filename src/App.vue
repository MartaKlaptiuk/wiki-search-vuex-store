<template>
  <div id="app">
    <header>
      <search></search>
    </header>

    <main>
      <results></results>
    </main>
  </div>
</template>

<script>
import Search from "./components/Search";
import Results from "./components/Results";

export default {
  name: "App",
  components: {
    Search,
    Results
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 0;
  padding: 0;
}
</style>
