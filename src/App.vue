<template>
  <div id="app">
    <Header />
    <ProductList />
  </div>
</template>

<script>
import Header from "./components/Header";
import ProductList from "./components/ProductList";

export default {
  name: "App",
  components: {
    Header,
    ProductList,
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
}
</style>
