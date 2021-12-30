<template>
  <div class="container">
    <Header></Header>
    <hr>
    <div class="row">
      <Item v-for="index in 5" :key="index"> {{ index }}</Item>
      <ItemDetail></ItemDetail>
    </div>
    <hr>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from "./Header";
import Item from "./Item";
import ItemDetail from "./ItemDetail";
import Footer from "./Footer";

export default {
  name: "Odev",
  components: {
    Header,
    Item,
    ItemDetail,
    Footer,
  }
}
</script>

<style scoped>

</style>
