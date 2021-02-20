<template>
  <!-- <v-carousel>
      <v-carousel-item
            :v-for="(itemnextArtistImagei) in artistImagesList"
            :key="i"
            ><img :src="nextArtistImage.image_url" :alt="nextArtistImage.image_url"/>
      </v-carousel-item>
</v-carousel> -->

  <v-carousel
    cycle
    hide-delimiter-background
    show-arrows-on-hover
    :show-arrows="false"
  >
    <v-carousel-item v-for="item in meetups" :key="item.id">
      <img :src="item.image" class="img1" />
      <!-- <v-sheet :color="colors[i]" height="100%"> -->
      <!-- <v-row class="fill-height" align="center" justify="center"> -->
      <!-- <div class="display-3">{{ slide }} Slide</div> -->
      <!-- </v-row> -->
      <!-- </v-sheet> -->
    </v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
  data() {
    return {
      colors: [
        "indigo",
        "warning",
        "pink darken-2",
        "red lighten-1",
        "deep-purple accent-4",
      ],
      slides: ["First", "Second", "Third", "Fourth", "Fifth"],
      meetups: [
        {
          id: "1",
          image:
            "https://cdn.shopify.com/s/files/1/0046/2140/2241/files/Bioderma_for_Desktop--Slider-Design_1400x.jpg?v=1608099766",
        },
        {
          id: "2",
          image:
            "https://cdn.shopify.com/s/files/1/0046/2140/2241/files/Chrstmas-Main-Desktop-Slider-Design_1400x.jpg?v=1608097497",
        },
        {
          id: "3",
          image:
            "https://cdn.shopify.com/s/files/1/0046/2140/2241/files/Unilever_promotion_-_website_banner_1400x.jpg?v=1600938997",
        },
      ],
    };
  },
};
</script>

<style scoped>
.img1 {
  width: 100%;
  height: 30%;
}
</style>