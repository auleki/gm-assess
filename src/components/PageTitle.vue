<script>
export default {
  name: "PageTitle",
  props: {
    title: String
  }
}
</script>

<template>
  <div class="title">
    <h2>{{title}}</h2>
    <div class="line"></div>
  </div>
</template>

<style lang="scss" scoped>
.title {
  // background: #e9e9e9;
  margin: 1em 0;
  display: inline-flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

h2 {
  padding: .5em;
}

.line {
  width: 5rem;
  height: .2rem;
  background: #1a1a1a;
}
</style>