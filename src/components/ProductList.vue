<template>
  <ul>
    <li v-for="product in products" :key="product.id">
      <ProductCard :product="product" @add-to-cart="addToCart" />
    </li>
  </ul>
</template>

<script>
import ProductCard from './ProductCard.vue';
import { ref } from 'vue';

export default {
  components: { ProductCard },
  setup() {
    const products = ref([
      { id: 1, name: 'Product 1', price: 10.00 },
      { id: 2, name: 'Product 2', price: 15.00 },
      // Add more products to the array
    ]);

    const addToCart = (product) => {
      // Logic to add product to cart (implement later)
      console.log('Adding product to cart:', product);
    };

    return { products, addToCart };
  },
};
</script>
