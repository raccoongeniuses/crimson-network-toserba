<template>
  <div>
    <nav class="navbar navbar-light bg-light">
      <span class="navbar-brand mb-0 h1">Toserba Bule Jaksel</span>
      <span class="navbar-brand mb-0 h1">Cart ({{ totalQty }})</span>
    </nav>
  </div>
</template>

<style scoped>
nav {
  margin-bottom: 50px;
}
</style>
<script>
import { mapGetters } from "vuex";

export default {
  name: "HeaderComponent",
  computed: {
    ...mapGetters(["cart"]),
    totalQty() {
      return this.cart.reduce((a, b) => a + b.qty, 0);
    },
  },
};
</script>
