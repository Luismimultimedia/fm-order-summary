<template>
  <main class="home-page">
    <order-summary-card-component
      title="Order Summary"
      description="You can now listen to millions of songs, audiobooks, and podcasts on any device anywhere you like!"
      titlePlan="Annual Plan"
      pricePlan="59.99"
      successTextAction="Proceed to Payment"
      cancelTextAction="Cancel Order"
    />
  </main>
</template>

<script>
import OrderSummaryCardComponent from '../components/orderSummaryCard/OrderSummaryCardComponent';

export default {
  components: { OrderSummaryCardComponent },
  name: 'Home',
}
</script>

<style lang="scss">
@import url('../styles/global.scss');
.home-page {
  align-items: center;
  background-image: url("/assets/images/pattern-background-desktop.svg");
  background-repeat: no-repeat;
  background-size: contain;
  display: flex;
  height: 100vh;
  justify-content: center;
  width: 100%;
  @media (max-width: 425px) {
    background-image: url("/assets/images/pattern-background-mobile.svg");
  }
}
</style>