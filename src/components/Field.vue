<template>
  <b-field v-bind="{ ...$props, ...$attrs }">
    <b-input icon="account" value="Kevin Garvey" />
  </b-field>
</template>

<script>
export default {};
</script>

<style lang="sass" scoped>
.field
  margin-right: 15px
  ::v-deep
    .label
      color: #4B504C
    input
      border-radius: 10px
      background: #FFFFFF
      border: 1px solid #878787
      box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.25)
      border-radius: 10px
      color: #4B504C
</style>
