<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
    <!-- <Baitap1 /> -->
    <!-- <Baitap2 /> -->
    <!-- <DataBinding /> -->
    <!-- <Computed /> -->
    <!-- <Directive /> -->
    <!-- <ExampleDirective /> -->
    <!-- <User /> -->
    <BookingBus />
  </div>
</template>

<script>
// import Baitap1 from "./baitap1";
// import Baitap2 from "./baitap2";
// import DataBinding from "./data-binding";
// import Computed from "./computed";
// import Directive from "./directive";
// import ExampleDirective from "./directive/example";
// import User from "./components/user";
import BookingBus from "./booking-bus";

export default {
  name: "App",
  components: {
    //     Baitap1,
    //     Baitap2,
    //     DataBinding,
    //     Computed,
    //     Directive,
    //     ExampleDirective,
    // User,
    BookingBus
  }
};
</script>

<style lang="scss">
.title {
  color: red;
}
</style>
