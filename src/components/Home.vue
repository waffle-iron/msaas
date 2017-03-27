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
        </div>
      </div>
    </main>
    <!--/Main layout-->
  </div>
</template>

<script>
import HeaderComponent from '@/components/Header'

export default {
  components: {
    HeaderComponent,
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
</style>
