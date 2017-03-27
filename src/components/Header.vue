<template>
  <header>
      <!-- Sidebar navigation -->
      <sidebar-compoenent></sidebar-compoenent>
      <!--/. Sidebar navigation -->

      <!--Navbar-->
      <navbar-component></navbar-component>
      <!--/.Navbar-->
  </header>
</template>

<script>
import SidebarComponent from '@/components/layout/Sidebar'
import NavbarComponent from '@/components/layout/Navbar'

export default {
  components: {
    SidebarComponent, NavbarComponent,
  },
}
</script>

<style lang="css">
</style>
