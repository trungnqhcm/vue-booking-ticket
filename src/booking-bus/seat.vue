<template>
  <div>
    <button
      class="btn btn-default"
      :class="{ active: seat.TrangThai }"
      v-on="seat"
      @click="bookTicket"
    >{{ seat.SoGhe }}</button>
  </div>
</template>

<script>
export default {
  props: ["seat"],
  data() {
    return {};
  },
  methods: {
    bookTicket() {
      this.$emit("eventBookTicket", this.seat);
    }
  }
};
</script>

<style>
.btn {
  margin: 4px;
  flex: 0 1 auto;
}

.btn.active {
  background-color: lightgreen;
}
</style>