<template>
  <div class="card-teaser">
    <img :src="imageUrl" alt="Teaser Image" class="teaser-image" />
    <div class="teaser-content">
      <h3>{{ headline }}</h3>
      <p>{{ body }}</p>
    </div>
  </div>
</template>

<script setup>
import { defineProps } from "vue";

const props = defineProps({
  imageUrl: String,
  headline: String,
  body: String,
});
</script>

<style scoped>
.card-teaser {
  width: 100%; /* To fill out the content area */
  display: flex;
  flex-direction: column;
  padding: 0;
  margin: 15px;
}

.teaser-image {
  width: 100%;
  max-width: 500px; /* Adjust max-width as needed */
  margin-bottom: 20px; /* Adjust the bottom margin to control space between image and headline */
}

.teaser-content h3 {
  margin-top: 0; /* Removes the top margin from the headline */
  margin-bottom: 10px; /* Adjust the bottom margin to control space between headline and body text */
}

.teaser-content p {
  margin-top: 0; /* Removes the top margin from the paragraph, reducing space between it and the headline */
}
</style>
