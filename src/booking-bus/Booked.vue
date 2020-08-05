<template>
  <div>
    <ul v>
      <li v-bind:key="seat.Soghe" v-for="seat in bookedSeats">{{seat.TrangThai}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "bookedSeats",
  props: ["seats"],
  computed: {
    bookedSeats: function() {
      return this.seats.filter(function(seat) {
        return seat.TrangThai;
      });
    }
  }
};
</script>

<style>
</style>