<template>
  <div id="app">
    <div class="router">
      <router-link class="router" to="/">Home</router-link> |
      <router-link class="router" to="/todo">Todo List</router-link>
    </div>
    <router-view />
  </div>
</template>

<style scoped>
#app {
  margin-top: 50px;
}
.router {
  text-decoration: none;
  color: #333333;
  text-align: center;
}
.router-link-exact-active {
  color: #0067bc;
  font-weight: bold;
}
</style>
