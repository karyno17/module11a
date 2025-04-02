<template>
  <div id="app">
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/random-facts">Random Jokes</router-link> |
      <router-link to="/contact">Contact</router-link>
    </nav>

    <router-view />
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#app {
 font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #f0e6ff; /* light text for contrast */
  background-color: #2e003e; /* dark purple background */
  min-height: 100vh;
  padding-top: 40px;

  nav {
  margin-bottom: 30px;
  }

router-link {
  margin: 0 12px;
  font-weight: bold;
  text-decoration: none;
  color: #d8b4f8;
  }

router-link:hover {
  color: #ffffff;
  }
}

nav {
  margin-bottom: 20px;
}

router-link {
  margin: 0 10px;
}
</style>

