<template>
  <div>
    <button>{{name}}</button>
  </div>
</template>

<script>
export default {
  props: ["name"]
};
</script>

<style>
button {
  width: 32px;
  height: 32px;
  align-content: center;
}
.btn.active {
  background-color: red;
}
</style>