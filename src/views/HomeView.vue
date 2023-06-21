<template>
  <div class="home">

      <!-- <div class="row">
        <div class="coupon-box">COUPON Saving up to 25%</div>
        <div class="coupon-box">Free Delivery For spending up $100</div>
        <div class="coupon-box">GOLD MEMBRSHIP up to 50%</div>
      </div> -->
    <div class="warpper">
      <div class="bargen-box">
      <h2 class="">SPRING SALE — 20% OFF WITH CODE: SPRING 
        <RouterLink to="/product">SHOP NOW</RouterLink></h2>
    </div>
    <div class="show-product">
      <center>
        <div class="p-i">

        </div>
      </center>
    </div>
    <div class="list-product">
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
  </div>
    
     
  </div>
</template>

<script>
import jsonData from './DataAPI/dataAPI.json'; 

export default {
  data() {
    return {
      products: []
    };
  },
  mounted() {
    this.products = jsonData;
  }
};

</script>


<!-- style scoped on data API -->
<!-- body style -->
<style>
.home{
  margin-top: 70px;
  display: block;
  
  
}

/* h2 {
  margin: 0;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
} */
.show-product{
  margin-top: 15px;
}
.p-i{
      width: 98%;
      height: 500px;
      border-radius: 5px;
      /* background-color: #bfa; */
      background-image: url(../assets/images/leo.jpg);
      text-align: center;
      padding: 20px;
      font-size: 18px;
      font-weight: bold;
}
.bargen-box {
      width: 100%;
      height: 100px;
      border: 1px solid #000;
      background-color: #bfa;
      text-align: center;
      padding: 20px;
      font-size: 18px;
      font-weight: bold;
    }

@media (min-width: 2048px) {
  .home {
    min-height: 100vh;
    display: flex;
    flex-direction: row;
    align-items: center;
  }

}


</style>
