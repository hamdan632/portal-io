<template>
  <v-container class="">
    <div style="margin-left: 10%;">
      <v-col >
        <v-card-title>Game Guides</v-card-title>
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
              <v-row style="background-color: #121212">
                <game-guide-component title="Statistics" description="View all the stats in detail on click" icon="mdi-chart-bar"></game-guide-component>
                <game-guide-component title="Pro Build" description="View all the stats in detail on click" icon="mdi-folder"></game-guide-component>
                <game-guide-component title="Tier List" description="View all the stats in detail on click" icon="mdi-play-circle-outline"></game-guide-component>
              </v-row>
              <v-card-title class="screen-back-color mt-5">
                <v-icon>mdi-account</v-icon>
                <span class="ml-2">Valorant</span>
              </v-card-title>
              <v-row style="background-color: #121212">
                <game-guide-child-image-component title="Comps" description="View all the data on click of this component" ></game-guide-child-image-component>
                <game-guide-component title="Pro Build" description="View all the stats in detail on click" icon="mdi-folder"></game-guide-component>
                <game-guide-component title="Tier List" description="View all the stats in detail on click" icon="mdi-play-circle-outline"></game-guide-component>
                <game-guide-component title="Pro Build" description="View all the stats in detail on click" icon="mdi-folder"></game-guide-component>
                <game-guide-component title="Statistics" description="View all the stats in detail on click" icon="mdi-chart-bar"></game-guide-component>
              </v-row>
              <v-card-title class="screen-back-color mt-5">
                <v-icon>mdi-account</v-icon>
                <span class="ml-2">Teamfight Tactics</span>
              </v-card-title>
              <v-row style="background-color: #121212">
                <game-guide-component title="Pro Build" description="View all the stats in detail on click" icon="mdi-folder"></game-guide-component>
                <game-guide-component title="Tier List" description="View all the stats in detail on click" icon="mdi-play-circle-outline"></game-guide-component>
                <game-guide-component title="Pro Build" description="View all the stats in detail on click" icon="mdi-folder"></game-guide-component>
                <game-guide-component title="Statistics" description="View all the stats in detail on click" icon="mdi-chart-bar"></game-guide-component>
                <game-guide-component title="Tier List" description="View all the stats in detail on click" icon="mdi-play-circle-outline"></game-guide-component>
              </v-row>
            </v-card>
            <v-card v-if="tab.title === 'Leagues of Legends'">
              <v-row class="mt-10">
                <game-guide-component title="Statistics" description="View all the stats in detail on click" icon="mdi-chart-bar"></game-guide-component>
                <game-guide-component title="Pro Build" description="View all the stats in detail on click" icon="mdi-folder"></game-guide-component>
                <game-guide-component title="Tier List" description="View all the stats in detail on click" icon="mdi-play-circle-outline"></game-guide-component>
              </v-row>
            </v-card>
            <v-card v-if="tab.title === 'Teamfight Tactics'">
              <v-row class="mt-10">
                <game-guide-child-image-component title="Comps" description="View all the data on click of this component" ></game-guide-child-image-component>
                <game-guide-component title="Pro Build" description="View all the stats in detail on click" icon="mdi-folder"></game-guide-component>
                <game-guide-component title="Tier List" description="View all the stats in detail on click" icon="mdi-play-circle-outline"></game-guide-component>
                <game-guide-component title="Pro Build" description="View all the stats in detail on click" icon="mdi-folder"></game-guide-component>
                <game-guide-component title="Statistics" description="View all the stats in detail on click" icon="mdi-chart-bar"></game-guide-component>
                <game-guide-component title="Tier List" description="View all the stats in detail on click" icon="mdi-play-circle-outline"></game-guide-component>
              </v-row>
            </v-card>
            <v-card v-if="tab.title === 'Valorant'">
              <v-row class="mt-10">
                <game-guide-component title="Pro Build" description="View all the stats in detail on click" icon="mdi-folder"></game-guide-component>
                <game-guide-component title="Tier List" description="View all the stats in detail on click" icon="mdi-play-circle-outline"></game-guide-component>
                <game-guide-component title="Pro Build" description="View all the stats in detail on click" icon="mdi-folder"></game-guide-component>
                <game-guide-component title="Statistics" description="View all the stats in detail on click" icon="mdi-chart-bar"></game-guide-component>
                <game-guide-component title="Statistics" description="View all the stats in detail on click" icon="mdi-chart-bar"></game-guide-component>
                <game-guide-component title="Statistics" description="View all the stats in detail on click" icon="mdi-chart-bar"></game-guide-component>
              </v-row>
            </v-card>
            <v-card v-if="tab.title === 'CS:GO'">
              <v-row class="mt-7 d-flex justify-center" style="background-color: #121212">
                <v-card-text class="text-center mt-10" >
                  We do not have any Game Guides for
                  <span class="font-weight-bold">
                     Counter Strike: Global Offensive
                  </span>
                  yet
                </v-card-text>
                <v-btn text class="ma-6 black--text" style="background-color: #989595">
                  Explore game guides for other games
                </v-btn>
              </v-row>
            </v-card>
            <v-card v-if="tab.title === 'Apex Legends'">
              <v-row class="mt-10 d-flex justify-center" style="background-color: #121212">
                <v-card-text class="text-center mt-10" >
                  We do not have any Game Guides for
                  <span class="font-weight-bold">
                     Apex Legends
                  </span>
                  yet
                </v-card-text>
                <v-btn text class="ma-6 black--text" style="background-color: #989595">
                  Explore game guides for other games
                </v-btn>
              </v-row>
            </v-card>


          </v-tab-item>
        </v-tabs>
      </v-col>
    </div>
  </v-container>
</template>

<script>
import gameGuideComponent from "../components/gameGuideComponent.vue";
import gameGuideChildImageComponent from "../components/gameGuideChildImageComponent.vue";
export default {
  layout: 'detailsPage',
  components:{
    gameGuideComponent,
    gameGuideChildImageComponent
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
