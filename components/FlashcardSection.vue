<template>
  
    
    <div class="flashcard-container">
            <header class="flashcard-header">
            <h2 class="flashcard-title">Headline flashcards - examples - 4 columns</h2>
            <p class="flashcard-description">Optional text here.</p>
            </header>
                <div class="flashcard-grid">
                    <FlipCard v-for="card in cards" :key="card.id">
                        <template #front>
                        <h4 class="flashcard-item-title">{{ card.frontTitle }}</h4>
                        <img :src="card.frontImageUrl" alt="Frontside flashcard icon" class="flashcard-item-icon" />
                        </template>
                        <template #back>
                        <h4 class="flashcard-item-title">{{ card.backTitle }}</h4>
                        <img :src="card.backImageUrl" alt="Backside flashcard icon" class="flashcard-item-icon" />
                        </template>
                    </FlipCard>
                </div>
    </div>
      

  
  </template>
  
  <script setup>
  import FlipCard from '~/components/FlipCard.vue';
  import { ref } from 'vue';
  
  const cards = ref([
    {
      id: 1,
      frontTitle: 'Frontside 1000',
      frontImageUrl: 'https://cdn.builder.io/api/v1/image/assets/TEMP/f39820b56241e07d8c556f89f2823e835fc02af5089d3bfd09896fb7e3e97cb5?apiKey=cedf3aae0bf94bc7986d9fc56f4beb47&',
      backTitle: 'Backside 2000',
      backImageUrl: 'https://cdn.builder.io/api/v1/image/assets/TEMP/8a3ca379dc7f042fa3a9052b45e260e1c618ea958bbf643e925a5087886e6736?apiKey=cedf3aae0bf94bc7986d9fc56f4beb47&'
    },
    {
      id: 2,
      frontTitle: 'Frontside 1000',
      frontImageUrl: 'https://cdn.builder.io/api/v1/image/assets/TEMP/f39820b56241e07d8c556f89f2823e835fc02af5089d3bfd09896fb7e3e97cb5?apiKey=cedf3aae0bf94bc7986d9fc56f4beb47&',
      backTitle: 'Backside 2000',
      backImageUrl: 'https://cdn.builder.io/api/v1/image/assets/TEMP/8a3ca379dc7f042fa3a9052b45e260e1c618ea958bbf643e925a5087886e6736?apiKey=cedf3aae0bf94bc7986d9fc56f4beb47&'
    },
    {
      id: 3,
      frontTitle: 'Frontside 1000',
      frontImageUrl: 'https://cdn.builder.io/api/v1/image/assets/TEMP/f39820b56241e07d8c556f89f2823e835fc02af5089d3bfd09896fb7e3e97cb5?apiKey=cedf3aae0bf94bc7986d9fc56f4beb47&',
      backTitle: 'Backside 2000',
      backImageUrl: 'https://cdn.builder.io/api/v1/image/assets/TEMP/8a3ca379dc7f042fa3a9052b45e260e1c618ea958bbf643e925a5087886e6736?apiKey=cedf3aae0bf94bc7986d9fc56f4beb47&'
    },
    {
      id: 4,
      frontTitle: 'Frontside 1000',
      frontImageUrl: 'https://cdn.builder.io/api/v1/image/assets/TEMP/f39820b56241e07d8c556f89f2823e835fc02af5089d3bfd09896fb7e3e97cb5?apiKey=cedf3aae0bf94bc7986d9fc56f4beb47&',
      backTitle: 'Backside 2000',
      backImageUrl: 'https://cdn.builder.io/api/v1/image/assets/TEMP/8a3ca379dc7f042fa3a9052b45e260e1c618ea958bbf643e925a5087886e6736?apiKey=cedf3aae0bf94bc7986d9fc56f4beb47&'
    },
    // Add more cards as needed
  ]);
  </script>
  
  <style scoped>
 
h4 {
 color: aquamarine;
}
    
.flashcard-section {
  width: 984px; /* Ensure the section takes the full width */
}

.flashcard-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 20px;
}

.flip-card {
  cursor: pointer;

}

/* Additional styles to ensure .wrapper fills its container */
html, body {
  height: 100%;
  margin: 0;
}


  </style>
  