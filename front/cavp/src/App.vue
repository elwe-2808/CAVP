<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style lang="scss">
  @import "styles/normalize.css";

  $phone: 576px;
  $tablets: 768px;
  $desktop: 992px;
  $large-desktop: 1200px;
  $larger-desktop: 1400px;
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
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
  color: #42b983;
}
</style>
