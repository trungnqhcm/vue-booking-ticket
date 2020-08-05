<template>
  <div class="component">
    <h3>You may view the User Details here</h3>
    <p>Many Detail</p>
    <p>User name: {{name}}</p>
    <p>User age: {{age}}</p>
    <button class="btn btn-info mr-3" @click="resetName">Reset name</button>
  </div>
</template>

<script>
export default {
  props: ["name", "age"],
  methods: {
    resetName() {
      this.$emit("eventReset", "Nguyen");
      console.log("resetName -> this", this);
    }
  }
};
</script>

<style scoped>
div {
  background-color: lightcoral !important;
}
</style>