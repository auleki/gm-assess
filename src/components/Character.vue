<script>
export default {
  name: "Character",
}
</script>

<template>
  <div class="character">
    <img src="../assets/luke.png" alt="character">
    <section class="info">
      <h3 class="name">Luke Skywalker</h3>
      <span class="aka">Son of Anakin</span>
      <p class="about">
        Luke Skywalker a force sensitive human male, was a legendary Jedi Master who
        fought in the Galactic Civil War during the region of the Galactic empire
      </p>
      <p class="read__more">Read More</p>
    </section>
  </div>
</template>

<style lang="scss" scoped>
.character {
  background: #F2F2F2;
  flex: 1 35rem;
  display: inline-flex;
}

.read__more {
  border-bottom: .2rem solid #1a1a1a;
  display: inline-flex;
}
</style>