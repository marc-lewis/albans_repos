<template>
  <div>
    <alban-hero />
    <squatted-companies />
    <repos-for-sale />
    <testimonials />
  </div>
</template>

<script>
import AlbanHero from '~/components/AlbanHero/AlbanHero.vue'
import SquattedCompanies from '~/components/SquattedCompanies/SquattedCompanies.vue'
import ReposForSale from '~/components/ReposForSale/ReposForSale.vue'
import Testimonials from '~/components/Testimonials/Testimonials.vue'

export default {
  components: {
    AlbanHero,
    SquattedCompanies,
    ReposForSale,
    Testimonials
  }
}
</script>

<style>

</style>
