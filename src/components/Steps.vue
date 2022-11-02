<template>
  <section>
    <b-steps
      v-model="activeStep"
      :animated="true"
      :rounded="true"
      :mobile-mode="mobileMode"
    >
      <b-step-item step="1" label="Register" />

      <b-step-item step="2" label="Payment" />

      <b-step-item step="3" label="Confirmation" />
    </b-steps>
  </section>
</template>

<script>
export default {
  data() {
    return {
      activeStep: 1,
      labelPosition: "bottom",
      mobileMode: screen.width > "compact",
    };
  },
};
</script>

<style lang="sass" scoped>
.b-steps
    ::v-deep
      .step-navigation
        display: none
      .step-content
        display: none !important
      .step-items, .is-previous
        .step-item
          .step-link
            .step-marker
              border: none
              background-color: #9B2DCF !important
            .step-details
              display: none !important
        .is-active
          .step-marker
            border: 2px solid #000 !important
            color: #FFF !important
</style>
