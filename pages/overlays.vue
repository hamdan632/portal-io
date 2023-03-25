<template>
  <v-container class="">
    <div style="margin-left: 10%;">
      <v-col >
        <v-card-title>Overlays</v-card-title>
        <v-tabs
          style="max-width: 70%"
          centered v-model="tab" color="primary" slider-color="accent">
          <v-tab
            v-for="(tab, index) in tabs" :key="index">{{ tab.title }}</v-tab>
          <v-tab-item v-for="(tab, index) in tabs" :key="index">
            <v-card v-if="tab.title === 'All Games'">
              <v-card-title class="screen-back-color mt-5">
                <v-icon>mdi-account</v-icon>
                <span class="ml-2">Leagues of Legends</span>
              </v-card-title>
              <v-row>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
              </v-row>
              <v-card-title class="screen-back-color mt-5">
                <v-icon>mdi-account</v-icon>
                <span class="ml-2">Valorant</span>
              </v-card-title>
              <v-row>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
              </v-row>
              <v-card-title class="screen-back-color mt-5">
                <v-icon>mdi-account</v-icon>
                <span class="ml-2">CS:GO</span>
              </v-card-title>
              <v-row>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
              </v-row>
              <v-card-title class="screen-back-color mt-5">
                <v-icon>mdi-account</v-icon>
                <span class="ml-2">Apex Legends</span>
              </v-card-title>
              <v-row>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
              </v-row>
              <v-card-title class="screen-back-color mt-5">
                <v-icon>mdi-account</v-icon>
                <span class="ml-2">Teamfight Tactics</span>
              </v-card-title>
              <v-row>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
              </v-row>
            </v-card>
            <v-card v-if="tab.title === 'Leagues of Legends'">
              <v-row class="mt-10">
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
              </v-row>
            </v-card>
            <v-card v-if="tab.title === 'Teamfight Tactics'">
              <v-row class="mt-10">
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
              </v-row>
            </v-card>
            <v-card v-if="tab.title === 'Valorant'">
              <v-row class="mt-10">
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
              </v-row>
            </v-card>
            <v-card v-if="tab.title === 'CS:GO'">
              <v-row class="mt-10">
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
              </v-row>
            </v-card>
            <v-card v-if="tab.title === 'Apex Legends'">
              <v-row class="mt-10">
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
                <single-game-detail></single-game-detail>
              </v-row>
            </v-card>


          </v-tab-item>
        </v-tabs>
      </v-col>
    </div>
  </v-container>
</template>

<script>
import singleGameDetail from "../components/singleGameDetail.vue";
export default {
  layout: 'detailsPage',
  components:{
    singleGameDetail
  },
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
