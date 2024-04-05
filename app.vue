<template>
  <div>
    <TeaserList :teasers="teasersData" />
  </div>
</template>

<script>
import TeaserList from "~/components/ColumnGrid.vue";

export default {
  components: {
    TeaserList,
  },
  data() {
    return {
      teasersData: [
        {
          imageUrl: "/imageTest.png",
          headline: "Teaser 1 Headline",
          body: "This is an example of using 1px/5 cm wide walls . Here the robot is correctly localized: The red dots from the scanner data align with the black lines from the map",
        },
        {
          imageUrl: "/imageTest.png",
          headline: "Teaser 2 Headline",
          body: "Here, the thick wall to the right causes the robot to place itself too far to the right. Similarly, the thick wall at the top displaces it too far towards the top of the map. ",
        },
        {
          imageUrl: "/imageTest.png",
          headline: "Teaser 1 Headline",
          body: "An example of how using walls that are too thick can cause a localization error. THe robot tries to localize itself by placing as many of the red dots as possible inside the black area.",
        },
        {
          imageUrl: "/imageTest.png",
          headline: "Teaser 1 Headline",
          body: "An example of how using walls that are too thick can cause a localization error. THe robot tries to localize itself by placing as many of the red dots as possible inside the black area.",
        },

        // Add more teasers as needed
      ],
    };
  },
};
</script>
