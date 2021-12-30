<template>
  <div>
    <p> From parent component : {{ name}}</p>
    <p> reverse name from  parent component : {{ reverseName()}}</p>
  </div>
</template>

<script>

export default {
  props: {
    name: {
      type: String,
      default: "fuck",
    }
  },
  methods: {
    reverseName(){
      return this.name.split('').reverse().join('')
    }
  }
}
</script>


