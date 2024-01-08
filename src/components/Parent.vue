<template>
  <div>
    <p>Parent component</p>
    <button @click="showChild = !showChild">Toggle Child</button>
    <ChildCom v-if="showChild" @childFormSubmit="handleChildFormSubmit" />
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
  methods: {
    handleChildFormSubmit(dataFromChild) {
      // Handle the form submission data from ChildCom
      console.log("Form data received in ParentCom:", dataFromChild);
    },
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
