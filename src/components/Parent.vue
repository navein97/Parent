<template>
  <div>
    <p class="green">ParentCom component</p>
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

  beforeUpdate() {
    console.log("ParentCom beforeUpdate()");
  },
  updated() {
    console.log("ParentCom updated()");
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
