<template>
  <div class="green">Child component</div>
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

  beforeUnmount() {
    console.log("ChildCom beforeUnmount()");
  },
  unmounted() {
    console.log("ChildCom unmounted()");
  },
};
</script>

<!-- style scoped you dont pinjam the style to other components -->
<!-- If not, -->
<!-- They could potentially affect the entire application -->
<style scoped>
.green {
  color: rgb(106, 0, 255);
  font-weight: bold;
}
</style>
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
