<template>
  <ul class="list-group">
    <li class="list-group-item" v-for="item in cart" :key="item.id">
      <button
        type="button"
        class="close"
        data-dismiss="modal"
        aria-label="Close"
      >
        <span aria-hidden="true">&times;</span>
      </button>
      <div class="media">
        <img width="80px" src="item.imgUrl" class="mr-3" alt="item.title" />
        <div class="media-body">
          <p class="mt-0">{{ item.title }}</p>
          <button class="btn-qty btn btn-sm btn-secondary">-</button>
          x {{ item.qty }}
          <button class="btn-qty btn btn-sm btn-secondary">+</button>
        </div>
      </div>
    </li>
  </ul>
</template>

<script>
import { mapGetters } from "vuex";

export default {
  computed: {
    ...mapGetters(["cart"]),
  },
  name: "CartComponent",
};
</script>

<style scoped>
.btn-qty {
  border-radius: 50%;
  width: 30px;
}

.media {
  width: 90%;
}
.media-body {
  text-align: left;
}
</style>
