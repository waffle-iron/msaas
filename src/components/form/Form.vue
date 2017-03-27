<template>

  <form>

    <div v-for="elem in elements">

      <div v-if="elem.tipo === 'input'">
          <input-Component :psLabel="elem.label" :psType="elem.type" :psPlaceholder="elem.placeholder" ></input-Component>
      </div>
      <div v-else-if="elem.tipo === 'textArea'">
        <textArea-Component :psLabel="elem.label" :psRows="elem.row"></textArea-Component>
      </div>
      <div v-else-if="elem.tipo === 'select'">
        <select-Component :psLabel="elem.label" :psItens="elem.itens"></select-Component>
      </div>

    </div>

  </form>

</template>

<script>

  import InputComponent from './Input'
  import TextAreaComponent from './TextArea'
  import SelectComponent from './Select'

  export default {
    components: {
      InputComponent,
      TextAreaComponent,
      SelectComponent,
    },
    props: {
      elements:
      {
        type: Object,
        required: true,
      },
    },
  }
</script>

<style lang="css">
</style>
