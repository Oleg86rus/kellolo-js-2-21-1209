<template>
  <div>
    <div class="feturedItem">
      <div class="feturedItem fetured_items__link">
        <div class="feturedImgWrap">
          <div class="feturedBuy">
            <button
                class="hover_cart"
                name="add"
                @click="$parent.$parent.$refs.basket.add(item)"
            >
              <i class="fas fa-shopping-cart"></i> Add to Cart
            </button>
          </div>
          <img class="feturedProduct" :src="item.productImg" alt="product1">
        </div>
        <div>
          <div class="feturedBuySm d-flex flex-column justify-content-around align-items-center align-items-md-start">
            <div class="feturedItemName">{{ item.productName }}</div>
            <div class="feturedItemPrice price">${{ item.productPrice }}</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    item: {
      type: Object
    }
  }
}

</script>

<style>

</style>