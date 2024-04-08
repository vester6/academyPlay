<template>
  <div class="flip-card" @click="toggleFlip">
    <div class="flip-card-inner" :class="{ flipped: isFlipped.value }">
      <div class="flip-card-front">
        <img
          v-if="frontImageUrl"
          :src="frontImageUrl"
          alt="Front Image"
          class="card-image"
        />
        <p class="card-text">{{ frontText }}</p>
      </div>
      <div class="flip-card-back">
        <img
          v-if="backImageUrl"
          :src="backImageUrl"
          alt="Back Image"
          class="card-image"
        />
        <p class="card-text">{{ backText }}</p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const isFlipped = ref(false);

// Props
const frontImageUrl = undefined; // Optional
const frontText = String;
const backImageUrl = undefined; // Optional
const backText = String;

const toggleFlip = () => {
  isFlipped.value = !isFlipped.value;
};
</script>

<style scoped>
.flip-card {
  width: 100%;
  perspective: 1000px; /* Add perspective for 3D effect */
}

.flip-card-inner {
  width: 100%;
  height: 100%;
  transition: transform 0.6s;
  transform-style: preserve-3d; /* Preserve 3D effects */
}

.flip-card-inner.flipped {
  transform: rotateY(180deg); /* Rotate the inner card */
}

.flip-card-front,
.flip-card-back {
  width: 100%;
  height: 100%;
  position: absolute;
  backface-visibility: hidden; /* Hide the back of the card */
}

.card-image {
  width: 100%;
  height: auto;
}

.card-text {
  text-align: center;
  padding: 20px;
  font-size: 16px;
}
</style>
