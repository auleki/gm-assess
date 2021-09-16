<script>
import Character from '@/components/Character.vue'
import PageTitle from '@/components/PageTitle.vue'
export default {
  name: "Characters",
  components: {
    Character, 
    PageTitle
  }
}
</script>

<template>
  <div class="page">
    <PageTitle title="Starwars Characters"/>
    <section class="characters__section">
      <Character />
      <Character />
      <Character />
      <Character />
      <Character />
      <Character />
    </section>
  </div>
</template>

<style lang="scss" scoped>
.characters__section {
  display: flex;
  flex-wrap: wrap;
  padding: 0 1rem;
  row-gap: 1em;
  column-gap: .5em;
}
</style>