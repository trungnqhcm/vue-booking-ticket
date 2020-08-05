<template>
  <div>
    <h3 class="title">*Directive</h3>
    <div v-if="status">Cybersoft</div>
    <div v-else>Cybersoft 2</div>
    <button class="btn btn-success" @click="status = !status">Toggle</button>
    <div v-if="type === 'A'">A</div>
    <div v-else-if="type === 'B'">B</div>
    <div v-else-if="type === 'C'">C</div>
    <div v-else>ABCDEF</div>
    <div v-show="show">Demo v-show</div>

    <ul v-if="persons && persons.length > 0">
      <li
        v-for="(person, index) in persons"
        :key="index"
      >{{person.name}} - {{person.age}} - {{person.color}}</li>
    </ul>

    <template v-if="people">
      <div v-for="(value, key, index) in people" :key="index">{{key}} - {{value}}</div>
    </template>

    <h3 class="title">Class Binding</h3>
    <div class="demo" :class="divClass" @click="statusClass = !statusClass">Cybersoft</div>
    <div class="demo" :class="[activeClass, errClass]">Cybersoft</div>
    <h3 class="title">Style Binding</h3>
    <div class="demo" :style="myStyle"></div>
    <div class="demo" :style="[myStyle, {height: '200px'}]"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      status: true,
      type: "we",
      show: false,
      persons: [
        { name: "Nguyen", age: 18, color: "red" },
        { name: "Khai", age: 30, color: "pink" },
        { name: "Dan", age: 35, color: "blue" }
      ],
      people: { name: "Nguyen", age: 18, color: "red" },
      statusClass: true,
      activeClass: "active",
      errClass: "text-danger",
      color: "blue",
      width: "200"
    };
  },
  computed: {
    divClass() {
      return {
        red: this.statusClass,
        text: this.statusClass
      };
    },
    myStyle() {
      return {
        backgroundColor: this.color,
        width: this.width + "px"
      };
    }
  }
};
</script>

<style>
.demo {
  width: 100px;
  height: 100px;
  background-color: grey;
  margin: 10px;
}
.red {
  background-color: red;
}
.text {
  color: white;
  text-align: center;
  line-height: 100px;
}
.active {
  background-color: yellow;
}
.text-danger {
  color: red;
}
</style>