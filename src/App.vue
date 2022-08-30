<template>
  <Todolist />
</template>

<script>
//import HelloWorldVue from "./components/HelloWorld.vue";
import Todolist from "./components/todolist.vue";
export default {
  name: "App",
  components: {
    //HelloWorld: HelloWorldVue,
    Todolist,
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
