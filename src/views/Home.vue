<template>
  <div class="home">
    <EntityListing title="Popular Warships" />
    <!-- <EntityListing title="Popular Planets" />
    <EntityListing title="Popular Characters" /> -->
  </div>
</template>

<script>
import EntityListing from "@/components/EntityListing.vue";

export default {
  name: "Home",
  components: {
    EntityListing,
  },
};
</script>
