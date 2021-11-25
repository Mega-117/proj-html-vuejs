<template>
  <div class="row gy-3" :class="columnNumber">
    <div v-for="(element, i) in products" :key="i" class="col">
      <div class="card-product">
        <div class="img-product">
          <div v-if="element.sale === true" class="sale">
            <span>Sale!</span>
          </div>
          <div
            v-if="element.textOverlay2 || element.textOverlay"
            class="overlay-product"
          >
            <div v-if="element.textOverlay2" class="overlay-product-2">
              <h4>{{ element.text }}</h4>
              <span>{{ element.textOverlay2 }}</span>
            </div>

            <div v-if="element.textOverlay">
              <div class="circle">
                <i class="fa fa-check-square-o" aria-hidden="true"></i>
              </div>
              <div class="cart-text">
                <span>{{ element.textOverlay }}</span>
              </div>
            </div>
          </div>
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
.overlay-product {
  display: none;
  position: absolute;

  background-color: #a45f4267;
  width: 100%;
  height: 100%;
  .overlay-product-2 {
    color: white;
    height: 100%;
    display: flex;
    align-items: center;
    flex-direction: column;
    justify-content: center;
    padding: 0 20px;
    h4 {
      text-align: center;
    }
    span {
      font-size: 18px;
    }
  }
  .circle {
    position: absolute;
    top: 50%;
    left: 50%;
    width: 100px;
    height: 100px;
    transform: translate(-50%, -50%);
    background-color: rgba(0, 0, 0, 0.7);
    border-radius: 50%;
    color: white;
    text-align: center;
    line-height: 100px;
    font-size: 40px;
  }
  .cart-text {
    position: absolute;
    top: 70%;
    left: 50%;
    transform: translateX(-50%);
    color: white;
    font-size: 24px;
  }
}
.img-product {
  margin-bottom: 33px;
  position: relative;
  img {
    width: 100%;
  }
  .sale {
    position: absolute;
    top: 20px;
    left: 15px;
    padding: 5px 10px;
    color: white;
    background-color: #3d6f42;
    border-radius: 50%;
    font-size: 20px;
  }
}
.img-product:hover .overlay-product {
  display: block;
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