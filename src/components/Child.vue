<template>
  <div>Child component</div>
</template>

<script>
export default {
  name: "ChildCom",
  beforeCreate() {
    console.log("ChildCom beforeCreate()");
  },
  created() {
    console.log("ChildCom created()");
  },
  beforeMount() {
    console.log("ChildCom beforeMount()");
  },
  mounted() {
    console.log("ChildCom mounted()");
  },
  beforeUpdate() {
    console.log("ChildCom beforeUpdate()");
  },
  updated() {
    console.log("ChildCom updated()");
  },
  beforeUnmount() {
    console.log("ChildCom beforeUnmount()");
  },
  unmounted() {
    console.log("ChildCom unmounted()");
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
