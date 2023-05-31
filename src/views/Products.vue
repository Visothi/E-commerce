<template>
  <!-- <div class="product">
    <h1>This is an Product page</h1>
  </div> -->
  <div class="card">
    <ul class="product-list">
      <li v-for="product in products" :key="product.id" class="product-item">
        <div class="product-image">
          <img :src="product.image" :alt="product.title" />
        </div>
        <div class="product-details">
          <h3>{{ product.title }}</h3>
          <p class="product-price">Price: ${{ product.price }}</p>
          <p class="product-category">Category: {{ product.category }}</p>
          <p class="product-description">Description: {{ product.description }}</p>
          <button class="add-to-cart-button" @click="addToCart(product)">Add to Cart</button>

        </div>
      </li>
    </ul>
  </div>
</template>
<script>
import axios from 'axios';

export default {
  data() {
    return {
      products: []
    };
  },
  mounted() {
    axios
      .get('https://fakestoreapi.com/products')
      .then(response => {
        this.products = response.data;
      })
      .catch(error => {
        console.error(error);
      });
  }
};
</script>

<style>
@media (min-width: 1024px) {
  .product {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
.card{
  margin-top: 80px;
}
</style>
