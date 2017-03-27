<template>
  <nav class="navbar fixed-top navbar-toggleable-md navbar-dark scrolling-navbar double-nav">

      <!-- SideNav slide-out button -->
      <div class="float-left">
          <a href="#" data-activates="slide-out" class="button-collapse"><i class="fa fa-bars"></i></a>
      </div>

      <!-- Breadcrumb-->
      <div class="breadcrumb-dn mr-auto">
          <p>BrandFlow Home Page</p>
      </div>

      <ul class="nav navbar-nav nav-flex-icons ml-auto">
          <li class="nav-item">
              <a class="nav-link"> <span class="badge red z-depth-1">2</span> <i class="fa fa-shopping-cart"></i> <span class="hidden-sm-down">Cart</span></a>
          </li>
          <li class="nav-item">
              <a class="nav-link"><i class="fa fa-envelope"></i> <span class="hidden-sm-down">Contact</span></a>
          </li>
          <li class="nav-item">
              <a class="nav-link"><i class="fa fa-comments-o"></i> <span class="hidden-sm-down">Support</span></a>
          </li>
          <li class="nav-item">
              <a class="nav-link"><i class="fa fa-sign-in"></i> <span class="hidden-sm-down">Register</span></a>
          </li>
          <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                  <i class="fa fa-user"></i> <span class="hidden-sm-down">Profile</span>
              </a>
              <div class="dropdown-menu dropdown-menu-right" aria-labelledby="navbarDropdownMenuLink">
                  <a class="dropdown-item" href="#">Logout</a>
                  <a class="dropdown-item" href="#">My account</a>
              </div>
          </li>
      </ul>
  </nav>
</template>

<script>
  export default {

  }
</script>

<style lang="css">

</style>
