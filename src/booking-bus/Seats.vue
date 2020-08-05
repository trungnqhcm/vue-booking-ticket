<template>
  <div>
    <button
      class="btn"
      v-for="seat in seatsList"
      :key="seat.SoGhe"
      :class="{ active: seat.TrangThai }"
      @click="Choose"
    >{{ seat.SoGhe }}</button>
  </div>
</template>

<script>
export default {
  props: ["seatsList"],
  data() {},
  methods: {
    Choose: function() {
      this.$emit("update");
    }
  }
};
</script>

<style>
button {
  width: 32px;
  height: 32px;
  align-content: center;
}
.seat {
  margin: 2%;
}
.btn.active {
  background-color: red;
}
</style>