<template>
  <h2>{{ name }}</h2>
  <div>
    <p class="green">Child component</p>
    <form @submit.prevent="submitForm">
      <label for="childInput">Child Input:</label>
      <input v-model="formData" type="text" id="childInput" />
      <!-- v-model: what data is input, thats the data displayed -->
      <button v-on:click="changeName">Change name</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "ChildCom",
  data() {
    return {
      name: "Lee",
      formData: "",
    };
  },
  methods: {
    changeName() {
      // Update the name with the value from formData
      this.name = this.formData;
    },

    submitForm() {
      // Emit an event to the parent with the form data
      this.$emit("childFormSubmit", this.formData);
      // Reset the form data
      this.formData = "";
    },
  },
};
</script>

<!-- style scoped you dont pinjam the style to other components -->
<!-- If not, -->
<!-- They could potentially affect the entire application -->

<style scoped>
/* Template and Style Scoping */
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
