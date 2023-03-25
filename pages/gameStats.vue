<template>
      <v-container>
        <v-card class="ml-auto mr-auto">
          <v-card-title>{{ gameTitle }}</v-card-title>
          <v-card-subtitle>{{ gameSubtitle }}</v-card-subtitle>
          <v-card-text>{{ gameDescription }}</v-card-text>
          <!-- Your game details here -->
        </v-card>
        <v-card>
          <v-card-title>
            <v-tabs
              centered
              v-model="tab">
              <v-tab v-for="(item, index) in tabs" :key="index">
                {{ item.name }}
              </v-tab>
            </v-tabs>
          </v-card-title>
          <v-card-text>
            <v-tab-item v-for="(item, index) in tabs" :key="index">
              <v-container>
                <!-- Your tab content here -->
              </v-container>
            </v-tab-item>
          </v-card-text>
        </v-card>
      </v-container>
</template>

<script>
export default {
  layout: 'detailsPage',
  data() {
    return {
      title: "My App",
      color: "primary",
      elevation: 0,
      drawer: false,
      drawerIcon: "mdi-menu",
      gameTitle: "Game Title",
      gameSubtitle: "Game Subtitle",
      gameDescription: "Game Description",
      tab: 0,
      tabs: [
        { name: "Overview" },
        { name: "Pro Builds" },
        { name: "Trends" },
        { name: "Matchups & Counters" }
      ]
    };
  },
  methods: {
    toggleDrawer() {
      this.drawer = !this.drawer;
    }
  }
};
</script>

<style>
/* Add your custom styles here */
</style>
