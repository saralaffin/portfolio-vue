<template>
  <div id="app">
    <NavBar msg="Welcome to Your Vue.js App" />
    <Header />
  </div>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import Header from "./components/Header.vue";

export default {
  name: "App",
  components: {
    Header,
    NavBar,
  },
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  font-family: "Courier New", Courier, monospace;
}
</style>
