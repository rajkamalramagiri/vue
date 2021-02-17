<template>
  <div class="mx-auto overflow-hidden" height="400">
    <v-app-bar color="#070634" fixed>
      <v-app-bar-nav-icon @click="drawer = true" dark></v-app-bar-nav-icon>

      <div>
        <img
          class="sunnyLogo"
          src="https://cdn.shopify.com/s/files/1/0046/2140/2241/files/SUNNY_eSTORE_stacked_-white_60x.png?v=1590139908"
        />
      </div>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" absolute temporary>
      <v-list nav dense>
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-account</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Account</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
import "./Navigation.css";
export default {
  data: () => ({
    drawer: false,
    group: null,
  }),
};
</script>