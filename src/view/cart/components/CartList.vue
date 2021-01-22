<template>
  <div>
    <li v-for="product in products" :key="product.id">
      {{ product.title }}
      <button
        :disabled="product.inventory == 2"
        @click="deleteCartList(product)"
      >
        移除购物车
      </button>
    </li>
  </div>
</template>

<script>
export default {
  computed: {
    products() {
      return this.$store.state.products.all;
    }
  },
  methods: {
    deleteCartList(product) {
      this.$store.dispatch("cart/addCartList", product);
    },
  },
  created() {
    this.$store.dispatch("products/getAllProducts");
  }
};
</script>