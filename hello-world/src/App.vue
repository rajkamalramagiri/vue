<template>
  <div class="disableScroll">
    <Total />
    <Slider />

    <!-- <Navigation /> -->
    <!-- <Search /> -->
    <Courosal />

    <ProductSlider v-bind:todos="todos" />
    <ProductSlider v-bind:todos="todos" />
  </div>
</template>


<script>
// import Navigation from "./components/Navigation/Navigation";
// import Search from "./components/Search/Search";
import Courosal from "./components/Courosal";
import Total from "./components/Total";
import Slider from "./components/Slider";
import ProductSlider from "./components/ProductSlider";
export default {
  name: "App",
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "Todo One",
          completed: false,
          src:
            "https://cdn.shopify.com/s/files/1/0046/2140/2241/products/21000007165_7a69e51e-efbe-4783-b91f-90b4efcc76cf_200x.jpg?v=1611048557",
        },
        {
          id: 2,
          title: "Todo Two",
          completed: true,
          src:
            "https://cdn.shopify.com/s/files/1/0046/2140/2241/products/21000008058_730ce034-08d9-42da-9390-6c8cffaf19bd_200x.jpg?v=1611048969",
        },
        {
          id: 3,
          title: "Todo Three",
          completed: false,
          src:
            "https://cdn.shopify.com/s/files/1/0046/2140/2241/products/21000008142_0148895f-48a1-4d7f-81f8-deb65b2a6172_200x.jpg?v=1611048965",
        },

        {
          id: 4,
          title: "Todo Three",
          completed: false,
          src:
            "https://cdn.shopify.com/s/files/1/0046/2140/2241/products/21000007165_7a69e51e-efbe-4783-b91f-90b4efcc76cf_200x.jpg?v=1611048557",
        },
        {
          id: 5,
          title: "Todo Three",
          completed: false,
          src:
            "https://cdn.shopify.com/s/files/1/0046/2140/2241/products/cc_cbe47ffb-8a89-47a9-9f3b-ff70567a55ab_200x.jpg?v=1611042870",
        },
        {
          id: 6,
          title: "Todo Three",
          completed: false,
          src:
            "https://cdn.shopify.com/s/files/1/0046/2140/2241/products/21000007165_7a69e51e-efbe-4783-b91f-90b4efcc76cf_200x.jpg?v=1611048557",
        },
      ],
    };
  },

  components: {
    // Navigation,
    // Search,
    Courosal,
    Slider,
    Total,
    ProductSlider,
  },
};
</script>
<style scoped>
.disableScroll {
  overflow-y: hidden;
  overflow-x: hidden;
  background-color: #f4f6f7;
}
</style>