<template>
  <v-container>
    <h1 class="text-center">Overlays</h1>
    <v-tabs centered v-model="tab" color="primary" slider-color="accent">
      <v-tab v-for="(tab, index) in tabs" :key="index">{{ tab.title }}</v-tab>
      <v-tab-item v-for="(tab, index) in tabs" :key="index">
        <v-card v-if="tab.title === 'All Games'">
          <v-card-title>
            <v-icon>mdi-account</v-icon>
            <span class="ml-2">Leagues of Legends</span>
          </v-card-title>
        </v-card>
      </v-tab-item>
    </v-tabs>
  </v-container>
</template>

<script>
export default {
  layout: 'detailsPage',
  data() {
    return {
      tab: null,
      tabs: [
        { title: 'All Games' },
        { title: 'Leagues of Legends' },
        { title: 'Teamfight Tactics' },
        { title: 'Valorant' },
        { title: 'CS:GO' },
        { title: 'Apex Legends' },
      ],
    };
  },
};
</script>

<style scoped>
.text-center {
  text-align: center;
}
</style>
