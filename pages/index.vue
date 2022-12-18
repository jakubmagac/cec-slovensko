<template>
  <div>
    <about />
    <register />
    <location />
    <schedule />
    <workshop />
  </div>
</template>

<script>
import about from '../components/about.vue'
import Register from '../components/register.vue'
import Location from '../components/location.vue'
import Schedule from '../components/schedule.vue'
import Workshop from '../components/workshop.vue'

export default {
  name: 'IndexPage',
  components: { about, Register, Location, Schedule, Workshop }
}
</script>

<style lang="scss" scoped>
</style>
