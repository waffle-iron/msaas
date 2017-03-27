<template>

  <main class="col-sm-9 offset-sm-3 col-md-10 offset-md-2 pt-3">

    <div class="col-sm-4 col-md-5">
      <div class="card">
        <div class="card-block">
            <TvForm :elements="form1()"></TvForm>
        </div>
      </div>
    </div>

  </main>

</template>

<script>

  import TvForm from './form.vue'

  export default {
    components: {
      TvForm
    },
    methods: {
      form1 () {
        return {
          elements:
          [
            {
              tipo: 'input',
              label: 'Nome',
              type: 'text'
            },
            {
              tipo: 'texArea',
              label: 'Descrição',
              row: 4
            },
            {
              tipo: 'input',
              label: 'Senha',
              type: 'password'
            },
            {
              tipo: 'input',
              label: 'email',
              type: 'text'
            },
            {
              tipo: 'input',
              label: 'Idade',
              type: 'number'
            },
            {
              tipo: 'select',
              label: 'Sexo',
              itens: [
                {
                  value: 'm',
                  item: 'Masculino'
                },
                {
                  value: 'f',
                  item: 'Feminino'
                }
              ]
            }
          ]
        }
      }
    }
  }
</script>

<style lang="css">
  /* Placeholders */
  .placeholders {
    padding-bottom: 3rem;
  }

  .placeholder img {
    padding-top: 1.5rem;
    padding-bottom: 1.5rem;
  }
</style>
