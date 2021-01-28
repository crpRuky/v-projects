<template>
  <div id="app">
    <div id="nav">
      <router-link to="/on">On</router-link>&thinsp;
      <router-link to="/off">Off</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style>
body {
  background-color:black;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #959da7;
}

#nav {
  padding: 30px;
}

#nav a {
  font-size:24px;
  font-weight: bold;
  color: #959da7;
}

a {
  text-decoration:none;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
