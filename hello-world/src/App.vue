<template>
  <div>
    <Total />

    <!-- <Navigation /> -->
    <!-- <Search /> -->
    <Courosal />
  </div>
</template>


<script>
// import Navigation from "./components/Navigation/Navigation";
// import Search from "./components/Search/Search";
import Courosal from "./components/Courosal";
import Total from "./components/Total";
export default {
  name: "App",

  components: {
    // Navigation,
    // Search,
    Courosal,
    Total,
  },

  data: () => ({
    //
  }),
};
</script>
