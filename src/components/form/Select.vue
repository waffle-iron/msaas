<template>

  <div class="select-wrapper mdb-select" ref="divWidth">
    <span class="caret">▼</span>
    <input type="text" v-model="chooseSelected" class="select-dropdown" v-bind:class="{ active: isActive }" @click="toggleSelect" readonly="true"
    data-activates="select-options-4787c8f4-32a4-a17a-8ab3-463544f9c9bc"
    value="Selecione uma opção">
    <ul v-bind:class="{ active: isActive }" v-bind:style="{ display: activeDisplay, width: thisWith + 'px'}" id="select-options-4787c8f4-32a4-a17a-8ab3-463544f9c9bc"
    class="dropdown-content select-dropdown" style="width: 545.031px;
    position: absolute; top: 0px; left: 0px; opacity: 1; ">
      <li @click="toggleSelectItem" class="disabled"><span>Selecione uma opção</span></li>
      <li @click="toggleSelectItem">
        <input hidden type="text" value="descricao1">
        <span>Descrição 1</span>
      </li>
      <li @click="toggleSelectItem">
        <input hidden type="text" value="descricao2">
        <span>Descrição 2</span>
      </li>
      <li @click="toggleSelectItem">
        <input hidden type="text" value="descricao3">
        <span>Descrição 3</span>
      </li>
    </ul>
    <select class="mdb-select initialized">
        <option value="" disabled="" selected="">Choose your option</option>
        <option value="1">Option 1</option>
        <option value="2">Option 2</option>
        <option value="3">Option 3</option>
    </select>
    <label>{{psLabel}}</label>
  </div>

</template>

<script>
  export default {
    data () {
      return {
        isActive: false,
        activeDisplay: 'none',
        chooseSelected: 'Selecione uma opção',
        selectItemSelected: null,
        valueChooseSelected: null,
        divWidth: null,
        thisWith: 100
      }
    },
    methods: {
      toggleSelect () {
        this.isActive = !this.isActive
        this.thisWith = this.$refs.divWidth.offsetWidth
        if (this.isActive) {
          this.activeDisplay = 'block'
        } else {
          this.activeDisplay = 'none'
        }
      },
      toggleSelectItem (event) {
        this.toggleSelect()
        if (this.selectItemSelected != null) {
          this.selectItemSelected.className = ' '
        }
        event.srcElement.parentElement.className += ' active selected'
        this.selectItemSelected = event.srcElement.parentElement
        this.valueChooseSelected = event.srcElement.parentElement.firstElementChild.value
        this.chooseSelected = event.srcElement.innerText
      }
    },
    props: {
      psId:
      {
        type: String
      },
      psLabel:
      {
        required: true,
        type: String
      },
      psItens:
      {
        required: true,
        type: Array
      }
    }
  }
</script>

<style lang="css">

</style>
