<template>
  <div>
    ParentCom component
    <button @click="showChild = !showChild">Toggle Child</button>
    <ChildCom v-if="showChild" />
  </div>
</template>

<script>
import ChildCom from "./Child.vue";
export default {
  name: "ParentCom",
  components: { ChildCom },
  data() {
    return {
      showChild: true,
    };
  },
  beforeCreate() {
    console.log("ParentCom beforeCreate()");
  },
  created() {
    console.log("ParentCom created()");
  },
  beforeMount() {
    console.log("ParentCom beforeMount()");
  },
  mounted() {
    console.log("ParentCom mounted()");
  },
  beforeUpdate() {
    console.log("ParentCom beforeUpdate()");
  },
  updated() {
    console.log("ParentCom updated()");
  },
  beforeUnmount() {
    console.log("ParentCom beforeUnmount()");
  },
  unmounted() {
    console.log("ParentCom unmounted()");
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
