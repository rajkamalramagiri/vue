<template>
  <div>
    <div class="container-full">
      <div class="container">
        <div class="container-left">
          <v-list-item-icon>
            <v-icon class="white menu" @click="drawer = true">mdi-menu</v-icon>
          </v-list-item-icon>

          <img
            class="image"
            src="https://cdn.shopify.com/s/files/1/0046/2140/2241/files/SUNNY_eSTORE_stacked_-white_60x.png?v=1590139908"
          />
        </div>

        <div class="container-right">
          <v-list-item-icon>
            <v-icon class="white account">mdi-account-circle</v-icon>
          </v-list-item-icon>
          <v-list-item-icon>
            <v-icon class="white cart">mdi-cart-outline</v-icon>
          </v-list-item-icon>
        </div>
      </div>
      <div class="container-down">
        <v-text-field
          class="search"
          label="Search"
          solo
          hide-details
          clearable
        ></v-text-field>
      </div>
    </div>

    <v-navigation-drawer v-model="drawer" absolute temporary>
      <v-list class="listitems">
        <v-list-group
          v-for="item in items"
          :key="item.title"
          v-model="item.active"
          no-action
        >
          <template v-slot:activator>
            <v-list-item-content>
              <v-list-item-title v-text="item.title"></v-list-item-title>
            </v-list-item-content>
          </template>

          <v-list-item v-for="child in item.items" :key="child.title">
            <v-list-item-content>
              <v-list-item-title v-text="child.title"></v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-group>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<style scoped>
.container-full {
  width: 100%;

  background-color: #070634;
}

.container-down {
  color: white;
  padding: 15px;
  padding-top: 3px;
  padding-bottom: 10px;
}
.container {
  width: 100%;
  padding: 5px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.container-left {
  display: flex;
  align-items: center;
}
.image {
  width: 50px;
  height: 50px;
  object-fit: contain;
}

.white {
  color: white !important;
}
.account {
  color: white !important;
  margin-right: 10px;
}
.menu {
  margin-left: 8px;
  margin-right: 15px;
}
.cart {
  margin-right: 10px;
}
</style>


<script>
export default {
  data: () => ({
    drawer: false,
    group: null,
    items: [
      {
        items: [
          { title: "Android Phones" },
          { title: "iPhones" },
          { title: "Computers" },
          { title: "Tablets" },
        ],
        title: "Electronics",
      },
      {
        items: [
          { title: "Mobile accessories" },
          { title: "Computer accessories" },
          { title: "Camera accessories" },
          { title: "Audio" },
          { title: "Smart watches & accessories" },
          { title: "Travel accessories" },
          { title: "Other" },
        ],
        title: "Acessories & Gadgets",
      },
      {
        items: [
          { title: "Televisions" },
          { title: "Washers & Dryers" },
          { title: "Large Kitchen Appliances" },
          { title: "Small Kitchen Applicances" },
          { title: "Cooling & Air Quality" },
          { title: "Lightning Solutions" },
          { title: "Household Appliances" },
        ],
        title: "Home & Office Appliances",
      },
      {
        items: [
          { title: "Canned food" },
          { title: "Instant noodles" },
          { title: "Food Staples & Cooking Ingredients" },
          { title: "Dairy" },
          { title: "Snacks" },
          { title: "Coffee & Tea" },
          { title: "Non-alcoholic drinks" },
          { title: "Alcoholic drinks" },
        ],
        title: "Food & Drinks",
      },
      {
        items: [
          { title: "Bath & Kitchen" },
          { title: "Cleaning & Laundry" },
          { title: "Stationery" },
          { title: "Personal Care" },
          { title: "Women's Care" },
        ],
        title: "Household Essentials",
      },
      {
        items: [
          { title: "Health & Beauty" },
          { title: "Baby Care" },
          { title: "Medicines & Medical Supplies" },
          { title: "Supplements" },
          { title: "Bath & Body" },
          { title: "Makeup" },
          { title: "Skincare" },
          { title: "Haircare" },
          { title: "Fragrances" },
          { title: "Beauty Accessories" },
          { title: "Vitamins & Supplements" },
        ],
        title: "Health & Beauty",
      },
    ],
  }),
  methods: {
    click() {
      this.toggle = false;
    },
  },
};
</script>
