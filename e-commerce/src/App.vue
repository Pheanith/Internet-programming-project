<!-- <template>
  <h1>"This is my first VueJs project"</h1>
</template>  -->

<template>
  <div class="box">
    <div class="wrapper">
    <Categories v-for="i in Category" :key="i.Category"
   :bgcolor="i.bgcolor" 
            :image="i.image" 
            :Product="i.Product" 
            :quantity="i.quantity">

  </Categories>
  </div>
  <br>

  <div class="promotion-container">
    <Promotions v-for=" i in Promotion" :key="i.Promotion"
    :colorBackground="i.colorBackground"
    :description="i.description"
    :productImages="i.productImages"
    :btnbgcolor="i.btnbgcolor"
    :btntext="i.btntext">
    </Promotions>
  </div>
  </div>
  
  
  
</template>

<script>
import SuperProduct from "./views/SuperProduct.vue";
import Menu from "./components/menu.vue";
export default {
  name: "App",
  components: {
    SuperProduct,
    Menu,
  },
};
</script>

<style scoped>
.promotion-container{
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  /* justify-content: center;
  align-items: center; */
  gap: 32px;
}
.wrapper{
  display: flex;
  justify-content: center;
  align-items: center;
  
  gap: 32px;
}
.box{
  width: 1520px;
  margin: auto;

}
</style>
