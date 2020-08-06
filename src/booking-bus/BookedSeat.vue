<template>
  <li>
    <div>
      {{seat.TenGhe}} - {{seat.Gia}}
      <button
        class="btn btn-outline-danger btn-sm"
        @click="unBookTicket"
      >Huỷ</button>
      <br />
    </div>
  </li>
</template>

<script>
export default {
  props: ["seat"],
  methods: {
    unBookTicket() {
      this.$emit("eventUnBookTicket", this.seat);
    }
  }
};
</script>

<style>
</style>