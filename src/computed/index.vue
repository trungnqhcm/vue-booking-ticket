<template>
  <div>
    <h3 class="title">*Computed</h3>
    <div>{{compareMessage}} | {{counter}}</div>
    <button class="btn btn-success" @click="counter++">Increase</button>

    <div>{{result()}} | {{counterSecond}}</div>
    <button class="btn btn-success" @click="counterSecond++">Increase Second</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      counter: 0,
      counterSecond: 0
    };
  },
  computed: {
    compareMessage() {
      return this.counter > 5 ? "Lon hon 5" : "Be hon 5";
    }
  },

  methods: {
    result() {
      return this.counterSecond > 5 ? "Lon hon 5" : "Be hon 5";
    }
  },

  watch: {
    counter() {
      setTimeout(() => {
        this.counter = 0;
      }, 2000);
    }
  }
};
</script>

<style>
</style>