<template>
    <div>
    <b-navbar toggleable="lg" type="dark" variant="dark">
      <a class="navbar-brand">
        <img src="../assets/flower.png" alt="flower-icon" height="42" width="35">
      </a>
    <b-navbar-brand href="#" id="brand">Sci-Tings</b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
        <b-nav-item href="/" active-class="active">Home</b-nav-item>
        <b-nav-item href="explore" active-class="active">Explore Data</b-nav-item>
        <b-nav-item-dropdown text="Discussions" right>
          <b-dropdown-item href="#">Climate Change</b-dropdown-item>
          <b-dropdown-item href="#">Healthcare</b-dropdown-item>
          <b-dropdown-item href="#">Justice</b-dropdown-item>
          <b-dropdown-divider></b-dropdown-divider>
          <b-dropdown-item href="#">Data Repositories</b-dropdown-item>
        </b-nav-item-dropdown>
      </b-navbar-nav>


      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">
        <b-nav-item href="register">Sign Up</b-nav-item>
        <b-nav-item href="login">Log In</b-nav-item>
        <b-nav-form>
          <b-form-input size="sm" class="mr-sm-2" placeholder="Search Data"></b-form-input>
          <b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button>
        </b-nav-form>

      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</div>
</template>

<script>
export default {
  
}
</script>

<style scoped>
    #brand{
        color:#28a745;
    }
    .active{
      color:white;
    }
</style>