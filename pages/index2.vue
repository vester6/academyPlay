<template>
    <div>
        <NuxtLink to="/flipcardpage">Go to Flip Card Page</NuxtLink>
      <p>4 teasers</p>
      <TeaserList :teasers="teasersData" />
      <p>3 teasers</p>
      <TeaserList :teasers="teasersData2" />
      <p>2 teasers</p>
      <TeaserList :teasers="teasersData3" />
    </div>
  </template>
  
  <script setup>
  import { ref } from "vue";
  import TeaserList from "~/components/ColumnGrid.vue";
  
  // Define your reactive data using ref()
  const teasersData = ref([
    {
      imageUrl: "/imageTest.png",
      headline: "Teaser 1 Headline",
      body: "This is an example of using 1px/5 cm wide walls. Here the robot is correctly localized: The red dots from the scanner data align with the black lines from the map.",
    },
    {
      imageUrl: "/imageTest.png",
      headline: "Teaser 2 Headline",
      body: "Here, the thick wall to the right causes the robot to place itself too far to the right. Similarly, the thick wall at the top displaces it too far towards the top of the map.",
    },
    {
      imageUrl: "/imageTest.png",
      headline: "Teaser 3 Headline",
      body: "An example of how using walls that are too thick can cause a localization error. The robot tries to localize itself by placing as many of the red dots as possible inside the black area.",
    },
    {
      imageUrl: "/imageTest.png",
      headline: "Teaser 3 Headline",
      body: "An example of how using walls that are too thick can cause a localization error. The robot tries to localize itself by placing as many of the red dots as possible inside the black area.",
    },
    // Add more teasers as needed
  ]);
  const teasersData2 = ref([
    {
      imageUrl: "/imageTest.png",
      headline: "Teaser 31 Headline",
      body: "This is an example of using 1px/5 cm wide walls. Here the robot is correctly localized: The red dots from the scanner data align with the black lines from the map.",
    },
    {
      imageUrl: "/imageTest.png",
      headline: "Teaser 32 Headline",
      body: "Here, the thick wall to the right causes the robot to place itself too far to the right. Similarly, the thick wall at the top displaces it too far towards the top of the map.",
    },
    {
      imageUrl: "/imageTest.png",
      headline: "Teaser 33 Headline",
      body: "An example of how using walls that are too thick can cause a localization error. The robot tries to localize itself by placing as many of the red dots as possible inside the black area.",
    },
  
    // Add more teasers as needed
  ]);
  const teasersData3 = ref([
    {
      imageUrl: "/imageTest.png",
      headline: "Teaser 31 Headline",
      body: "This is an example of using 1px/5 cm wide walls. Here the robot is correctly localized: The red dots from the scanner data align with the black lines from the map.",
    },
    {
      imageUrl: "/imageTest.png",
      headline: "Teaser 32 Headline",
      body: "Here, the thick wall to the right causes the robot to place itself too far to the right. Similarly, the thick wall at the top displaces it too far towards the top of the map.",
    },
  
    // Add more teasers as needed
  ]);
  </script>
  