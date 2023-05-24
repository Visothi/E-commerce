<template>
  <div class="home">

    <div class="model">
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
    </div>
    <!-- <br>
    <div class="items" >
        <div class="item"><div class="box"><img src="../assets/images/item.jpg" alt=""></div></div>
        <div class="item"><div class="box"><img src="../assets/images/item.jpg" alt=""></div></div>
        <div class="item"><div class="box"><img src="../assets/images/item.jpg" alt=""></div></div>
        <div class="item"><div class="box"><img src="../assets/images/item.jpg" alt=""></div></div>
        <div class="item"><div class="box"><img src="../assets/images/item.jpg" alt=""></div></div>
        <div class="item"><div class="box"><img src="../assets/images/item.jpg" alt=""></div></div>
        <div class="item"><div class="box"><img src="../assets/images/item.jpg" alt=""></div></div>
        <div class="item"><div class="box"><img src="../assets/images/item.jpg" alt=""></div></div>
        <div class="item"><div class="box"><img src="../assets/images/item.jpg" alt=""></div></div>
        <div class="item"><div class="box"><img src="../assets/images/item.jpg" alt=""></div></div>
        <div class="item"><div class="box"><img src="../assets/images/item.jpg" alt=""></div></div>
        <div class="item"><div class="box"><img src="../assets/images/item.jpg" alt=""></div></div>
    </div>

    <br>
     -->
     <div>
    <!-- <h2>JSON Data:</h2> -->
    <ul>
      <li v-for="item in jsonData" :key="item.id">
        <p>{{ item.name }}</p>
        <p>{{ item.description }}</p>
      </li>
    </ul>
  </div>
      

  </div>
</template>
<script>
// export default {
//   mounted() {
//    const url = "https://fakestoreapi.com/products/1";
//    async function getAllProducts(){
//     const response = await fetch(url);
//     const data = await response.json();
//     console.log(data);
//    }
//    getAllProducts();
//   },
// };
export default {
  // data() {
  //   return {
  //     jsonData: [
  //       { id: 1, name: 'Item 1', description: 'Description for Item 1' },
  //       { id: 2, name: 'Item 2', description: 'Description for Item 2' },
  //       { id: 3, name: 'Item 3', description: 'Description for Item 3' }
  //     ]
  //   };
  // }

};

</script>

<style>

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
  display: block;
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
