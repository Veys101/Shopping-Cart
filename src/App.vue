<template>
  <nav>
    <router-link :class="{active: $route.name === 'home'}" to="/">Home</router-link> |
    <router-link :class="{active: $route.name === 'cart'}" to="/cart">Cart</router-link>
  </nav>
  <router-view/>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #384166;
}

html, body {
  margin: 0;
  padding: 0;
  overflow-x: hidden;
}

body {
  background-color: rgb(245, 245, 245);
}

nav {
  padding: 10px;
  width: 100%;
  height: 30px;
  background-color: rgb(48, 45, 45);
  line-height: 30px;
}

a {
  font-weight: bold;
  color: rgb(102, 97, 97);
  text-decoration: none;
  margin: 0 5px 0 5px;
  font-size: 1.25rem;

  &.active {
    color: #ffffff;
  }
}

.text-center {
  text-align: center;
}
</style>
