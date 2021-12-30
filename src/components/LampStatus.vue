<template>
  <div>
    <p>Lamba Situation is {{ status}}</p>
    <Button @click="changeStatus">Change Status</Button>
    <hr>
  </div>
</template>

<script>
export default {
  name: "LampStatus",

  data: function () {
    return {
      status: "ON ",

    }
  },
  methods: {
    changeStatus: function () {
      this.status = "OFF"
      console.log(this.status)
    }
  }
}
</script>

<style scoped>

</style>
