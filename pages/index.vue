<template>
  <div>
    <div class="container">
      <Hero />
      <div class="rootLargeCard">
        <LargeCardDisplay
          v-for="cardInfo in largeCardSections"
          :key="cardInfo.id"
          :cardsSection="cardInfo"
        />
      </div>
      <SmallCardDisplay
        v-for="cardInfo in smallCardSections"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
      />
    </div>
  </div>
</template>

<script>
// @ts-ignore
import { largeCardSections, smallCardSections } from "@/assets/data.js";
export default {
  data() {
    return {
      largeCardSections: largeCardSections,
      smallCardSections: smallCardSections,
    };
  },
};
</script>

<style scoped>
.rootLargeCard {
  margin-top: 20% !important;
}
</style>
