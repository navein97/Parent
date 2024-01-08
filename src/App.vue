<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <ParentCom />
  <!-- ParentCom in template = to connect with Parent.vue -->
  <!-- And then Parent.vue they import ChildCom, that's connection -->
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
  data() {
    return {
      // cant have brackets in between Lee
      // its
      names: ["Ali", "Lee", "Muthu"],
    };
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
  margin-top: 60px;
}
</style>
