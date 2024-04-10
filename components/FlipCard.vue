<template>
  <div class="flip" @click="toggleFlip">
    <div class="card" :class="{ flipped: isFlipped }">
      <div class="face front">
        <slot name="front">Front2</slot>
      </div>
      <div class="face back">
        <slot name="back">Back2</slot>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const isFlipped = ref(false);

function toggleFlip() {
  isFlipped.value = !isFlipped.value;
}
</script>

<style>
.flip {
  width: 100%; /* To fill out the content area */
  display: flex;
  flex-direction: column;
  padding: 0;
  margin: 15px;
  perspective: 800px;
  height: auto;
}

.flip .card.flipped {
  transform: rotateY(-180deg);
}

.flip .card {
  width: 100%;
  height: 100%;
  transform-style: preserve-3d;
  transition: transform 0.5s;
}




.flip .card .back {
  transform: rotateY(-180deg);
  
}

</style>
