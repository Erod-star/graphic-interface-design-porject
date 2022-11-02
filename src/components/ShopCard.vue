<template>
  <div class="shop-card">
    <div class="sc-details">
      <p class="d-title">Vintage wine</p>
      <p class="d-description">
        Lorem ipsum dolor sit amet, nor das dracarys ofmec
      </p>
    </div>
    <p class="sc-price">$49.99</p>
  </div>
</template>

<script>
export default {};
</script>

<style lang="sass" scoped>
.shop-card
    width: 100%
    height: 70px
    margin-bottom: 15px
    background: #ECECEC
    display: flex
    padding: 12px 10px
    border-radius: 10px
    justify-content: space-between
    overflow: hidden
    .sc-details
      .d-title
        text-align: center
        font-weight: 700
        color: #000
      .d-description
        color: #000

    .sc-price
      color: #9B2DCF
      font-weight: 700
      text-align: center
</style>
