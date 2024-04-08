<template>
  <div class="wrapper">
    <div class="flip-card-list">
      <FlipCard
        v-for="(card, index) in cards"
        :key="index"
        :front-image-url="card.frontImageUrl"
        :front-text="card.frontText"
        :back-image-url="card.backImageUrl"
        :back-text="card.backText"
      />
    </div>
  </div>
</template>

<script setup>
import FlipCard from "~/components/FlipCard.vue";
import { ref } from "vue";

// Sample cards data
const cards = ref([
  {
    frontImageUrl: "/imageTest.png",
    frontText: "Front text for card 1",
    backImageUrl: "/imageTest.png",
    backText: "Back text for card 1",
  },
  {
    frontImageUrl: "/imageTest.png",
    frontText: "Front text for card 2",
    backImageUrl: "/imageTest.png",
    backText: "Back text for card 2",
  },
  // Add more cards as needed
]);
</script>

<style scoped>
/* Styles remain the same */
</style>

<style scoped>
.flip-card-list {
  display: grid;
  gap: 20px;
  margin: 0 auto;
  max-width: 984px;
}

/* Define responsive layouts as needed */
</style>
