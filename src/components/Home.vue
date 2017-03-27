<template>
  <div>
    <!--Double navigation-->
    <header-component></header-component>
    <!--/Double navigation-->

    <!--Main layout-->
    <main>
      <div class="container-fluid">
        <div>
          <h1>Welcome to Your Vue.js App</h1>
          <h2>Essential Links</h2>
          <div class="col-md-6">
            <form-Component :elements="formElements"></form-Component>
          </div>
        </div>
      </div>
    </main>
    <!--/Main layout-->
  </div>
</template>

<script>
import HeaderComponent from '@/components/Header'
import FormComponent from '@/components/form/Form'

export default {
  components: {
    HeaderComponent,
    FormComponent,
  },
  data() {
    return {
      formElements:
      [
        {
          tipo: 'input',
          label: 'Nome',
          type: 'text',
        },
        {
          tipo: 'textArea',
          label: 'Descrição',
          row: 4,
        },
        {
          tipo: 'input',
          label: 'Senha',
          type: 'password',
        },
        {
          tipo: 'input',
          label: 'email',
          type: 'text',
        },
        {
          tipo: 'input',
          label: 'Idade',
          type: 'number',
        },
        {
          tipo: 'select',
          label: 'Sexo',
          itens: [
            {
              value: 'm',
              item: 'Masculino',
            },
            {
              value: 'f',
              item: 'Feminino',
            },
          ],
        },
      ],
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
</style>
