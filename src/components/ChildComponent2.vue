<template>
  <div class="mychild">
    <p> child component 2 </p>
    <p> age is : {{ age}} </p>
    <Button @click="sendAgeToParentComponent"> change age</Button>
  </div>
</template>

<script>
export default {
  name: "ChildComponent2",
  props: ["age"],
  methods: {
    sendAgeToParentComponent() {
      this.age = 30;
      this.$emit('ageEdited', this.age)
    }
  }
}
</script>

<style scoped>
.mychild {
  border: #2c3e50;
  text-align: center;
  margin-top: 30px;
  padding: 10px;
  box-shadow: 1px 1px 2px #666;
  background-color: aliceblue;
}
</style>
