<template>

  <div class="md-form">
    <textarea type="text" :id="psId" class="md-textarea"></textarea>
    <label :for="psId">{{psLabel}}</label>
  </div>

</template>

<script>
  export default {
    props: {
      psRows:
      {
        required: true,
        type: Number,
      },
      psId:
      {
        type: String,
      },
      psLabel:
      {
        type: String,
      },
    },
  }
</script>

<style lang="css">
</style>
