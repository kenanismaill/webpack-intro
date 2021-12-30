<template>
  <div class="child">
    <p> From parent component : {{ name }}</p>
    <p> age from parent component is : {{ age }}</p>
    <p> reverse name from parent component : {{ reverseName() }}</p>
    <Button @click="sendDataToparent"> send data to parent component</Button>
  </div>
</template>

<script>

export default {
  props: {
    name: {
      type: String,
      default: "fuck",
    },
    age:[String]
  },
  methods: {
    reverseName() {
      return this.name.split('').reverse().join('')
    },
    sendDataToparent() {
      this.$emit('data', 'bla bla data')
    }
  }
}
</script>

<style scoped>
.child {
  border: #2c3e50;
  text-align: center;
  margin-top: 30px;
  padding: 10px;
  box-shadow: 1px 1px 2px #666;
  background-color: aliceblue;
}
</style>
