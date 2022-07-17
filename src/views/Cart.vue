<template>
  <div class="cart">
    <h1>Your Cart</h1>
    <CartItemCard v-for="product in products" :key="product.id" :product="product"/>
    <CartSummaryPaymentCard />
  </div>
</template>

<script>
  import CartItemCard from '../components/CartItemCard.vue'
  import CartSummaryPaymentCard from '../components/CartSummaryPaymentCard.vue'

  export default {
    components: {
      CartItemCard,
      CartSummaryPaymentCard
    },
    computed: {
      products() {
        return this.$store.getters.cartItems
      }
    }
  }

</script>