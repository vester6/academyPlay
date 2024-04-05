<template>
  <div class="container">
    <TeaserList :teasers="teasers" />
  </div>
</template>

<script>
import TeaserList from "/components/TeaserList.vue";

export default {
  components: {
    TeaserList,
  },
  data() {
    return {
      teasers: [
        {
          image: "/imageTest.png",
          headline: "Headline 1",
          bodyText: "This is a sample teaser text for the first card.",
        },
        {
          image: "/imageTest.png",
          headline: "Headline 2",
          bodyText: "This is a sample teaser text for the second card.",
        },
        {
          image: "/imageTest.png",
          headline: "Headline 2",
          bodyText: "This is a sample teaser text for the second card.",
        },
        {
          image: "/imageTest.png",
          headline: "Headline 2",
          bodyText: "This is a sample teaser text for the second card.",
        }
        
        // Add more teaser objects as needed
      ],
    };
  },
};
</script>
