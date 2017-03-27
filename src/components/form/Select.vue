<template>

  <div>
    <label>{{ psLabel }}</label>
    <div class="select-wrapper mdb-select" ref="divWidth">
      <span class="caret">▼</span>
      <input type="text" v-model="chooseSelected" class="select-dropdown" v-bind:class="{ active: isActive }" @click="toggleSelect" readonly="true"
      data-activates="select-options-4787c8f4-32a4-a17a-8ab3-463544f9c9bc"
      value="Selecione uma opção">
      <ul v-bind:class="{ active: isActive }" v-bind:style="{ display: activeDisplay, width: thisWith + 'px'}" id="select-options-4787c8f4-32a4-a17a-8ab3-463544f9c9bc"
      class="dropdown-content select-dropdown" style="width: 545.031px;
      position: absolute; top: 0px; left: 0px; opacity: 1; ">
        <li @click="toggleSelectItem" class="disabled"><span>Selecione uma opção</span></li>
        <li @click="toggleSelectItem" v-for="item in psItens">
          <input hidden type="text" :value="item.value">
          <span>{{ item.item }}</span>
        </li>
      </ul>
    </div>
  </div>

</template>

<script>
  export default {
    data() {
      return {
        isActive: false,
        activeDisplay: 'none',
        chooseSelected: 'Selecione uma opção',
        selectItemSelected: null,
        valueChooseSelected: null,
        divWidth: null,
        thisWith: 100,
      }
    },
    methods: {
      toggleSelect() {
        this.isActive = !this.isActive
        this.thisWith = this.$refs.divWidth.offsetWidth
        if (this.isActive) {
          this.activeDisplay = 'block'
        } else {
          this.activeDisplay = 'none'
        }
      },
      toggleSelectItem(event) {
        this.toggleSelect()
        if (this.selectItemSelected != null) {
          this.selectItemSelected.className = ' '
        }
        // event.srcElement.parentElement.className += ' active selected'
        this.selectItemSelected = event.srcElement.parentElement
        this.valueChooseSelected = event.srcElement.parentElement.firstElementChild.value
        this.chooseSelected = event.srcElement.innerText
      },
    },
    props: {
      psId:
      {
        type: String,
      },
      psLabel:
      {
        required: true,
        type: String,
      },
      psItens:
      {
        required: true,
        type: Array,
      },
    },
  }
</script>

<style lang="css">

</style>
