<script>
import Warship from '@/components/Warship.vue'
import PageTitle from '@/components/PageTitle.vue'
export default {
  name: "Warships",
  components: {
    Warship,
    PageTitle
  }
};
</script>

<template>
  <div>
    <PageTitle title="Starwars Warship" />
    <Warship />
    <Warship />
    <Warship />
    <Warship />
    <Warship />
  </div>
</template>

<style lang="scss" scoped>
// styles
</style>