<template>
  <v-app-bar
    height="auto"
    class="py-12 text-white"
    style="box-shadow: none; background-color: #0a2458"
  >
    <!-- SinoAI Logo -->
    <v-img
      src="./../assets/sinoAI.png"
      :width="140"
      :height="192"
      @click.stop="drawer = !drawer"
    ></v-img>
    <!-- Navigation Menu -->
    <v-spacer></v-spacer>

    <template v-if="$vuetify.display.mdAndUp">
      <v-btn text class="px-6 text-subtitle-2 text-uppercase">Home</v-btn>
      <v-btn text class="px-6 text-subtitle-2 text-uppercase">About</v-btn>
      <v-btn text class="px-6 text-subtitle-2 text-uppercase">Database</v-btn>
      <v-btn text class="px-6 text-subtitle-2 text-uppercase">Insights</v-btn>
      <v-btn text class="px-6 text-subtitle-2 text-uppercase">Subscribe</v-btn>
    </template>
  </v-app-bar>

  <!-- Navigation Drawer for Mobile -->
  <v-navigation-drawer
    v-model="drawer"
    :location="$vuetify.display.mobile ? 'bottom' : undefined"
    temporary
  >
    <v-list :items="items"></v-list>
  </v-navigation-drawer>
</template>

<script>
export default {
  data: () => ({
    drawer: false,
    group: null,
    items: [
      { title: "Home", value: "home" },
      { title: "About", value: "about" },
      { title: "Database", value: "database" },
      { title: "Insights", value: "insights" },
      { title: "Subscribe", value: "subscribe" },
    ],
  }),

  watch: {
    group() {
      this.drawer = false;
    },
  },
};
</script>
