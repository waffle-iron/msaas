<template>

  <md-input-container>
    <label>{{psLabel}}</label>
    <md-input :placeholder="psPlaceholder"></md-input>
  </md-input-container>

</template>

<script>
  export default {
    props: {
      psLabel:
      {
        type: String
      },

      psType:
      {
        required: true,
        type: String
      },

      psId:
      {
        type: String
      },

      psPlaceholder:
      {
        type: String
      }
    }
  }
</script>

<style lang="css">
</style>
