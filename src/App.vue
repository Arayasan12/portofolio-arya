<template>
  <div id="app">
    <MenuUtama msg="Welcome to Your Vue.js" />
  </div>
</template>

<script>
import MenuUtama from "./components/MenuUtama.vue";

export default {
  name: "App",
  components: {
    MenuUtama,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
