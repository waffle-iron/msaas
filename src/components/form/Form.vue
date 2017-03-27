<template>

  <form>

    <div v-for="elem in elements.elements">

      <div v-if="elem.tipo === 'input'">
          <TvInputTxt :psLabel="elem.label" :psType="elem.type" :psPlaceholder="elem.placeholder" ></TvInputTxt>
      </div>
      <div v-else-if="elem.tipo === 'textArea'">
        <TvTextArea :psLabel="elem.label" :psRows="elem.row"></TvTextArea>
      </div>
      <div v-else-if="elem.tipo === 'select'">
        <TvSelect :psLabel="elem.label" :psItens="elem.itens"></TvSelect>
      </div>

    </div>

  </form>

</template>

<script>

  import TvInputTxt from './inputTxt.vue'
  import TvTextArea from './textArea.vue'
  import TvSelect from './select.vue'

  export default {
    components: {
      TvInputTxt,
      TvTextArea,
      TvSelect
    },
    props: {
      elements:
      {
        type: Object,
        required: true
      }
    }
  }
</script>

<style lang="css">
</style>
