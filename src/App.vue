<script>
import Navbar from "@/components/Navbar.vue";
import Header from "@/components/Header.vue";

export default {
  components: {
    Navbar,
    Header,
  },
};
</script>

<template>
  <Navbar
    :navLinks="[
      {
        name: 'Home',
        path: '/',
      },
      {
        name: 'Warships',
        path: '/warships',
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
  <Header />
  <router-view />
</template>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  border: 0;
}

.button {
  display: flex;
  background: #d8d8d8;
  padding: 1em 2em;
  cursor: pointer;
  transition: background 200ms ease-in-out, color 200ms ease-in-out;
  border-radius: 1px;
  &:hover {
    background: #1a1a1a;
    color: #fff;
  }
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
