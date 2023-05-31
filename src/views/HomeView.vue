<template>
  <div class="home">

    <!-- <div class="model" >
      <div class="row">
        <div class="coupon-box1">
          <h2 class="">SPRING SALE — 20% OFF WITH CODE: SPRING 
          <RouterLink to="/product">SHOP NOW</RouterLink></h2>
        </div>
      </div>
      <div class="row">
        <div class="coupon-box">COUPON Saving up to 25%</div>
        <div class="coupon-box">Free Delivery For spending up $100</div>
        <div class="coupon-box">GOLD MEMBRSHIP up to 50%</div>
      </div>
    </div> -->
    
    <div>
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
     
  </div>
</template>

<script>
import jsonData from './dataAPI.json';

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
.home{
  margin-top: 100px;
}

h2 {
  margin: 0;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
@media (min-width: 2048px) {
  .home {
    min-height: 100vh;
    display: flex;
    flex-direction: row;
    align-items: center;
  }

}



.model{
  width: 100%;
  height: auto;
  display: inline-block;
  /* flex-direction: row;
  justify-content: space-around; */
  margin-top: 50px;
}
.row{
  width: 100%;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;

  
}
.coupon-box1{
  /* background-color: */
  background-image: linear-gradient( 135deg, #FFF6B7 10%, #F6416C 100%);;
  position: relative;
  text-align: center;
  flex: 1;
  max-width: 100%;
  height: 80px;
  margin: 20px;
  border-radius: 10px;
  box-shadow: 0 0 5px rgba(181,225,235,255);
}
.coupon-box{
  /* background-color: rgba(181,225,235,255); */
  /* background-image: linear-gradient( 135deg, #FD6585 10%, #0D25B9 100%); */
  background-image: linear-gradient( 135deg, #69FF97 10%, #00E4FF 100%);
  position: relative;
  flex: 1;
  max-width: 400px;
  height: 200px;
  margin: 20px;
  border-radius: 10px;
  box-shadow: 0 0 5px rgba(181,225,235,255);
  font-family: Rockwell;
  font-size: 35px;
  text-align: center;
} @media (min-width: 2048px){
  .coupon-box{
    flex: 100%;
  
  }

  
}



</style>
