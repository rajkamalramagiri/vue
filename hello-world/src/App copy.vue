<template>
  <div>
    <Total />

    <!-- <Navigation /> -->
    <!-- <Search /> -->
    <Slider />

    <Courosal />
  </div>
</template  >


<script>
// import Navigation from "./components/Navigation/Navigation";
// import Search from "./components/Search/Search";
import Courosal from "./components/Courosal";
import Total from "./components/Total";
import Slider from "./components/Slider";
export default {
  name: "App",

  components: {
    // Navigation,
    // Search,
    Courosal,
    Total,
    Slider,
  },

  data: () => ({
    //
  }),
};
</script>
