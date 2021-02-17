<template>
  <div>
    <Navigation />
    <br />
    <br />
    <br />
    <Search />
  </div>
</template>

<script>
import Navigation from "./components/Navigation/Navigation";
import Search from "./components/Search/Search";
export default {
  name: "App",

  components: {
    Navigation,
    Search,
  },

  data: () => ({
    //
  }),
};
</script>
