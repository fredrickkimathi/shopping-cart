<template>
  <div class="product-card">
    <h3>{{ product.name }}</h3>
    <p>$${{ product.price }}</p>
    <button @click="$emit('add-to-cart', product)">Add to Cart</button>
  </div>
</template>

<script>
export default {
  props: {
    product: Object,
  },
};
</script>

<style scoped>
.product-card {
  /* Add product card styles (optional) */
}
</style>
