<template>
  <div class="row gy-3" :class="columnNumber">
    <div v-for="(element, i) in products" :key="i" class="col">
      <div class="card-product">
        <div class="img-product">
          <img :src="element.src" alt="" />
        </div>
        <div class="product-text" :class="element.alignText">
          <h5>{{ element.text }}</h5>
          <span v-if="element.scount" class="scount">{{ element.scount }}</span>
          <span class="price">{{ element.price }} {{ element.price2 }}</span>
          <span v-if="element.dataText" class="dataText">{{
            element.dataText
          }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardProduct",
  props: {
    products: Array,
    columnNumber: String,
  },
};
</script>

<style lang="scss">
.img-product {
  margin-bottom: 33px;
  img {
    width: 100%;
  }
}

.product-text {
  padding: 0 25px;
  margin-bottom: 35px;
  .scount {
    font-size: 12px;
    text-decoration: line-through;
    padding-right: 10px;
  }
  .price {
    color: green;
  }
  /* .dataText {
  } */
}
</style>