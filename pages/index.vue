<template>
  <div>
    <Nav />
    <div class="container">
      <Hero />
      <Large-card-display
        v-for="cardInfo in largeCardInfo"
        :key="cardInfo.id"
        :cards-section="cardInfo"
      />
      <Small-card-display
        v-for="cardInfo2 in smallCardSections"
        :key="cardInfo2.id"
        :cards-section="cardInfo2"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from '@/assets/data.js'
export default {
  data () {
    return {
      largeCardInfo: largeCardSections,
      smallCardSections
    }
  }
}
</script>

<style>
</style>
