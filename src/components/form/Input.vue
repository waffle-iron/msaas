<template>

  <div class="md-form">
    <input :type="psType" :id="psId" class="form-control">
    <label :for="psId" class="">{{psLabel}}</label>
  </div>

</template>

<script>
  export default {
    props: {
      psLabel:
      {
        type: String,
      },
      psType:
      {
        required: true,
        type: String,
      },
      psId:
      {
        type: String,
      },
      psPlaceholder:
      {
        type: String,
      },
    },
  }
</script>

<style lang="css">
</style>
