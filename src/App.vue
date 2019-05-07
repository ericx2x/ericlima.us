<template>
  <div id="app">
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/projects">Projects</router-link> |
      <router-link to="/resume">Resume</router-link>
    </div> -->
    <router-view />
  </div>
</template>

<script>
// export default{
//   methods: {
//     scrollProjects(){
//       alert();
//     }
//   },
// }
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Libre+Baskerville");
@import url("https://fonts.googleapis.com/css?family=Libre+Baskerville:400,400i,700");
@import url("https://fonts.google.com/specimen/Gothic+A1?selection.family=Gothic+A1:200,400,700,800");
@import url("https://fonts.googleapis.com/css?family=Montserrat:200,400,700,800");

@import "assets/css/flexboxgrid.css";

#app {
  /* font-family: "Avenir", Helvetica, Arial, sans-serif; */
  font-family: "Libre Baskerville", serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #1b98e0;
}
</style>
