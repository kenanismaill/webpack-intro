<template>
  <div id="app">
    <p> age is : {{ age }}</p>
    <p>data from child component is : {{ childData }}</p>
    <Button @click="changeName">Change title</Button>
    <HelloWorld :age="age" :name="title" @data="childData=$event"/>
    <ChildComponent2 @ageEdited="age= $event" :age="age"></ChildComponent2>

  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import ChildComponent2 from "./components/ChildComponent2";

export default {
  name: 'App',
  data: function () {
    return {
      title: "kenan",
      childData: "",
      age: 27
    }
  },
  methods: {
    changeName() {
      this.title = " New title"
    }
  },

  components: {
    HelloWorld,
    ChildComponent2,
  }
}
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
