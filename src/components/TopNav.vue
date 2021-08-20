<script>
export default {
  name: "TopNav",
};
</script>

<template>
  <nav>
    <div class="logo">
      <h1>STAR WARS</h1>
    </div>
    <div class="nav__links">
      <router-link to="/">STARSHIPS</router-link>
      <router-link to="/about">CHARACTERS</router-link>
    </div>
  </nav>
</template>



<style scoped lang="scss">
// use icons for links
nav {
  height: 100%;
  width: 100%;
  background: #1a1a1a;
  padding: 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 2em;

  .nav__links {
    display: flex;
    gap: 1em;
  }

  a {
    text-decoration: none;
    color: #fff;
    &.router-link-exact-active {
      color: crimson;
    }
  }
}
</style>