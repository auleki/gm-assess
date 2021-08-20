<script>
import ShipCard from "./ShipCard.vue";

export default {
  name: "EntityListing",
  props: {
    title: String,
  },
  components: {
    ShipCard,
  },
};
</script>

<template>
  <div>
    <div class="section__title">
      <h3>{{ title }}</h3>
    </div>
    <section class="container">
      <!-- A LIST OF ENTITIES -->
      <ShipCard />
      <ShipCard />
      <ShipCard />
      <ShipCard />
      <ShipCard />
      <ShipCard />
    </section>
  </div>
</template>

<style lang="scss" scoped>
.section__title {
  padding: 16px 0;
}
.container {
  display: grid;
  place-items: center;
  grid-template-columns: repeat(3, 3fr);
  gap: 2em;
}
</style>