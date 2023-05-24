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
<style scoped>
.product-list {
  list-style-type: none;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  padding: 0;
}

.product-item {
  width: 300px;
  background-color: #f5f5f5;
  border-radius: 8px;
  padding: 20px;
  margin-bottom: 20px;
}

.product-image img {
  width: 100%;
  border-radius: 4px;
  margin-bottom: 10px;
}

.product-details h3 {
  margin: 0;
  font-size: 20px;
  font-weight: bold;
}

.product-price {
  margin-top: 5px;
}

.product-category {
  margin-top: 5px;
  font-style: italic;
}

.product-description {
  margin-top: 10px;
}
</style>

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
