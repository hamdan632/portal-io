<template>
  <v-container>
    <v-tabs centered v-model="tab" color="primary" slider-color="accent">
      <v-tab  v-for="(tab, index) in tabs" :key="index">{{ tab.title }}</v-tab>
      <v-tab-item class="mt-10"  v-for="(tab, index) in tabs" :key="index">
          <general-settings v-if="tab.title === 'General settings'"></general-settings>
      </v-tab-item>
    </v-tabs>
  </v-container>
</template>

<script>
import generalSettings from "../components/generalSettings.vue";
export default {
  layout: 'detailsPage',
  components:{
    generalSettings
  },
  data() {
    return {
      tab: null,
      tabs: [
        { title: 'General settings' },
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
