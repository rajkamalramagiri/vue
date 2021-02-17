<template>
  <div>
    <Navigation />
    <br />
    <br />
    <br />
    <Search />
    <Courosal />
  </div>
</template>


<script>
import Navigation from "./components/Navigation/Navigation";
import Search from "./components/Search/Search";
import Courosal from "./components/Courosal";

export default {
  name: "App",

  components: {
    Navigation,
    Search,
    Courosal,
  },

  data: () => ({
    //
  }),
};
</script>
