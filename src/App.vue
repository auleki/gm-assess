<script>
import TopNav from "@/components/TopNav.vue";
import Navbar from "@/components/Navbar.vue";

export default {
  components: {
    TopNav,
    Navbar,
  },
};
</script>

<template>
  <Navbar
    :navLinks="[
      {
        name: 'Warships',
        path: '/',
      },
      {
        name: 'Characters',
        path: '/characters',
      },
      {
        name: 'About',
        path: '/about',
      },
    ]"
  />
  <router-view />
</template>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  border: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
