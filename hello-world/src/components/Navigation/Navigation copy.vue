<template>
  <div class="mx-auto overflow-hidden" height="400">
    <v-app-bar color="#070634" fixed>
      <v-app-bar-nav-icon @click="drawer = true" dark></v-app-bar-nav-icon>

      <img
        class="sunnyLogo"
        src="https://cdn.shopify.com/s/files/1/0046/2140/2241/files/SUNNY_eSTORE_stacked_-white_60x.png?v=1590139908"
      />
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" absolute temporary>
      <v-list>
        <v-list-item>
          <v-list-item-icon>
            <v-icon>mdi-home</v-icon>
          </v-list-item-icon>

          <v-list-item-title>Home</v-list-item-title>
        </v-list-item>

        <v-list-group :value="true" prepend-icon="mdi-account-circle">
          <template v-slot:activator>
            <v-list-item-title>Users</v-list-item-title>
          </template>

          <v-list-group :value="true" no-action sub-group>
            <template v-slot:activator>
              <v-list-item-content>
                <v-list-item-title>Admin</v-list-item-title>
              </v-list-item-content>
            </template>

            <v-list-item v-for="([title, icon], i) in admins" :key="i" link>
              <v-list-item-title v-text="title"></v-list-item-title>

              <v-list-item-icon>
                <v-icon v-text="icon"></v-icon>
              </v-list-item-icon>
            </v-list-item>
          </v-list-group>

          <v-list-group no-action sub-group>
            <template v-slot:activator>
              <v-list-item-content>
                <v-list-item-title>Actions</v-list-item-title>
              </v-list-item-content>
            </template>

            <v-list-item v-for="([title, icon], i) in cruds" :key="i" link>
              <v-list-item-title v-text="title"></v-list-item-title>

              <v-list-item-icon>
                <v-icon v-text="icon"></v-icon>
              </v-list-item-icon>
            </v-list-item>
          </v-list-group>
        </v-list-group>
      </v-list>
      <v-list>
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-title class="listitems" @click="click"
              >Electronics
            </v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title class="listitems"
              >Acessories & Gadgets</v-list-item-title
            >
          </v-list-item>

          <v-list-item>
            <v-list-item-title class="listitems"
              >Home & Office Appliances
            </v-list-item-title> </v-list-item
          ><v-list-item>
            <v-list-item-title class="listitems"
              >Food & Drinks</v-list-item-title
            > </v-list-item
          ><v-list-item>
            <v-list-item-title class="listitems"
              >Household Essentials</v-list-item-title
            > </v-list-item
          ><v-list-item>
            <v-list-item-title class="listitems"
              >Health & Beauty</v-list-item-title
            > </v-list-item
          ><v-list-item>
            <v-list-item-title class="listitems">Promotions</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>


<style scoped>
.listitems {
  font-family: "Roboto" !important;
}
</style>

<script>
import "./Navigation.css";
export default {
  data: () => ({
    drawer: false,
    group: null,
    admins: [
      ["Management", "mdi-account-multiple-outline"],
      ["Settings", "mdi-cog-outline"],
    ],
    cruds: [
      ["Create", "mdi-plus-outline"],
      ["Read", "mdi-file-outline"],
      ["Update", "mdi-update"],
      ["Delete", "mdi-delete"],
    ],
  }),
  methods: {
    click() {
      this.toggle = false;
    },
  },
};
</script>