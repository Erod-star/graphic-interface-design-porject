<template>
  <div id="layout" aria-label="layout">
    <div class="card">
      <Logo class="card-logo" />
      <div class="card-content">
        <div class="form-section">
          <h1 role="title" aria-label="section-subtitle">
            Welcome to the payment section!
          </h1>

          <div class="form-container">
            <form class="form">
              <Field class="owner-field" label="Owner" />
              <div class="card-container">
                <Field class="card-field" label="Card" />
                <img
                  class="card-image"
                  alt="card"
                  src="../assets/imgs/Cards.png"
                />
              </div>
              <div class="expiry-cvc">
                <Field class="expiry-field" label="Expiry" />
                <Field class="cvc-field" label="CVC" />
              </div>
            </form>
          </div>
        </div>

        <hr class="section-separator" />

        <div class="summary-section">
          <div class="summary-container">
            <h2>Summary</h2>
            <div class="summary-cards-container" focusable>
              <ShopCard />
              <ShopCard />
              <ShopCard />
              <ShopCard />
            </div>
            <div class="total-payment">
              <p class="mr-5">Total</p>
              <p>$249.99</p>
            </div>
          </div>

          <div class="buttons-container">
            <b-button type="is-primary">Go back</b-button>
            <b-button type="is-primary" class="ml-5">Submit </b-button>
          </div>
        </div>

        <div class="steps-indicators">
          <Steps />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { Field, ShopCard, Steps, Logo } from "@/components";

export default {
  components: {
    Field,
    ShopCard,
    Steps,
    Logo,
  },
  data() {
    return {
      oData: {},
    };
  },
};
</script>

<style lang="sass" scoped>
#layout
  min-height: 100%
  width: 100%
  display: flex
  flex-direction: column
  background: linear-gradient(to bottom, #0018B3, #9B2DCF)
  .card
    min-height: 100%
    height: calc( 100% - 120px )
    background: white
    border-radius: 30px
    display: flex
    flex-direction: column
    margin: 60px 27px
    .card-logo
      position: absolute
      left: calc(50% - 30px)
      top: -30px
    .card-content
      margin-top: 20px
      width: 100%
      h1
        text-align: center
        font-size: 1em
        font-weight: 600
        color: #000
        font-style: italic
      .form
        .field
          ::v-deep
            .label
              font-size: 0.75em
            input
              font-size: 0.75em
        .owner-field
          margin-right: 0px
        .card-container
          display: flex
          .card-field
            margin-right: 0px
            width: 60%
          .card-image
            margin-left: 20px
            width: 90px
            height: 90px
        .expiry-cvc
          display: flex
        .expiry-field, .cvc-field
          width: calc(33% - 15px)
    .summary-container
      border-top: 1px solid #878787
      border-bottom: 1px solid #878787
      h2
        text-align:  center
        font-size: 1.25em
        margin: 10px 0px
        color: #000
        font-weight: 500
      .summary-cards-container
        max-height: 130px
        overflow-y: scroll
        .shop-card
          ::v-deep
            .sc-details
              .d-title
                font-size: 0.87em
              .d-description
                font-size: 0.62em
            .sc-price
              font-size: 0.87em
      .total-payment
        display: flex
        justify-content: flex-end
        color: #000
        font-size: 1.125em
        font-weight: 500
        padding-top: 20px
        margin-bottom: 10px
    .buttons-container
      display: flex
      justify-content: space-between
      padding: 10px 25px
      button
        background: #9B2DCF !important
        box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25)
        border-radius: 25px
        font-weight: 600
        font-size: 0.875em
        width: 125px
        height: 40px
    .steps-indicators
      padding-top: 5px
    .section-separator
      display: none


// background-size: 400% 400%
// animation: animate-background 10s infinite ease-in-out

// @keyframes animate-background
//   0%,100%
//     background-position: 0 50%
//   50%
//     background-position: 100% 50%

@media only screen and (min-width: 700px)
  #layout
    padding: 50px 140px
    .card
      padding: 0px 35px
      .card-content
        .form
          .card-container
            display: flex
            .card-field
              margin-right: 0px
              margin-bottom: 0px
              width: 60%
            .card-image
              margin-left: 20px
              width: 100px
              height: 100px

@media only screen and (min-width: 1000px)
  #layout
    padding: 50px 0px
    .card
      .card-content
        display: flex
        justify-content: space-between
        .form-section
          .form
            margin-top: 15px
            width: 100%
            .owner-field
              width: 100%
            .card-container
              width: 400px
              .card-field
                margin-right: 0px
                margin-bottom: 0px
              .card-image
                margin-left: 40px
                width: 140px
                height: 140px
            .expiry-field, .cvc-field
              width: 120px
              position: absolute
              top: 220px
            .cvc-field
              left: 190px
      .steps-indicators
        position: absolute
        top: -85px
        width: 1050px
        left: calc(50% - 525px)
      .summary-container
        padding-left: 20px
        border-top: none
      .section-separator
        display: block
        width: 0.5px
        height: 265px
        background-color: #000
        margin: 0px
</style>
