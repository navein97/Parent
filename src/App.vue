<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <ParentCom />
</template>

<!-- Toggle On-->
<!-- Create and Mount and Update -->

<!-- Toggle Off-->
<!-- Unmount and Update -->

<!-- npm run serve -->

<script>
import ParentCom from "./components/Parent.vue";

export default {
  name: "App",
  components: { ParentCom },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
