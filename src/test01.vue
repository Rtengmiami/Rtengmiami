<template>
  <div>
    <h1>{{ title }}</h1>
    <button @click="changeTitle">改變按鈕</button>
    <div>{{ price }} x {{ quantity }} = {{ price * quantity }}</div>
  </div>
</template>

<script>
// import HelloWorldVue from "./components/HelloWorld.vue";
export default {
  name: "App",
  components: {},
  data: function () {
    return {
      title: "大標題",
      price: 10,
      quantity: 2,
    };
  },
  methods: {
    changeTitle() {
      this.title = "更改過囉";
    },
  },
};
</script>

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
