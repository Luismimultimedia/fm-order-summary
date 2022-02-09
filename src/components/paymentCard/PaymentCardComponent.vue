<template>
  <div class="payment-card__container">
      <img src="../../assets/images/icon-music.svg" class="payment-card__icon" />
      <div class="payment-card__information">
          <p>{{ titlePlan }}</p>
          <p>${{ pricePlan }}/year</p>
      </div>
      <a class="payment-card__change" href="" target="_blank">Change</a>
  </div>
</template>

<script>
export default {
    name: "PaymentCardComponent",
    props: {
        titlePlan: String,
        pricePlan: String,
    }
}
</script>

<style lang="scss">
    .payment-card {
        &__container {
            align-items: center;
            background-color: var(--color-very-pale-blue);
            border-radius: 10px;
            display: flex;
            margin: 1rem 0;
            padding: 1rem;
        }
        &__icon{
            float: left;
        }
        &__information {
            margin-left: 1rem;
            flex: 1;
            p {
                &:nth-child(1) {
                    color: var(--color-dark-blue);
                    font-size: 1.1rem;
                    font-weight: bold;
                }
                &:nth-child(2) {
                color: var(--color-desaturated-blue);
                font-size: 1rem;
            }
            }
        }
        &__change {
            color: var(--color-bright-blue);
            &:hover {
                color: hsl(245, 77%, 59%);
                text-decoration: none;
            }
        }
    }
</style>