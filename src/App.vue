<template>
  <div id="app"> 
    <my-nav></my-nav>
    <router-view/>
  </div>
</template>

<script>
import MyNav from './components/MyNav.vue';
export default {
  
  
  components: {
    myNav: MyNav
  }
}
</script>

<style>
html, body{
  height: 100%;
  margin: 0;
	padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color:#e9ecef;
  height: 100%;
  /* margin: 0; */
	/* padding: 0;  */
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
