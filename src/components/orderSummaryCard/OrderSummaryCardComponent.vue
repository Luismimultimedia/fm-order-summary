<template>
    <div class="order-summary-card__container">
      <figure class="order-summary-card__header">
            <img
                class="order-summary-card__header-img"
                src="../../assets/images/illustration-hero.svg"
            />
      </figure>
      <section class="order-summary-card__body">
          <h1 class="order-summary-card__body-title">{{ title }}</h1>
          <p class="order-summary-card__body-description">{{ description }}</p>
          <payment-card-component
            :titlePlan="titlePlan"
            :pricePlan="pricePlan"
          />
          <section class="order-summary-card__body-cta">
            <button-component :text="successTextAction" type="primary" />
            <button-component :text="cancelTextAction" type="secondary" />
          </section>
      </section>
    </div>
</template>

<script>
import PaymentCardComponent from "../paymentCard/PaymentCardComponent.vue";
import ButtonComponent from "../button/ButtonComponent.vue"

export default {
    name: "OrderSummaryCardComponent",
    components: {
        PaymentCardComponent,
        ButtonComponent,
    },
    props: {
        title: String,
        description: String,
        titlePlan: String,
        pricePlan: String,
        successTextAction: String,
        cancelTextAction: String
    }
}
</script>

<style lang="scss">
    .order-summary-card {
        &__container {
            border-radius: 10px;
            background-color: white;
            box-shadow: 0px 5px 11px -2px rgba(0,0,0,0.54);
            display: flex;
            flex-direction: column;
            width: 400px;
        }
        &__header {
            margin: 0;
            &-img {
                border-radius: 10px 10px 0px 0px;
                width: 100%;
            }
        }
        &__body {
            padding: 2rem;
            &-title {
                color: var(--color-dark-blue);
                font-size: 1.5rem;
                font-weight: bold;
                text-align: center;
            }
            &-description {
                color: var(--color-desaturated-blue);
                font-size: 1rem;
                font-weight: 400;
                text-align: center;
                margin-top: 1rem;
            }
            &-cta {
                display: flex;
                flex-direction: column;
            }
        }
    }
</style>