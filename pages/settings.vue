<template>
  <v-container>
    <div style="margin-left: 10%;">
      <v-col>
        <v-card-title>Settings</v-card-title>
        <v-tabs
          style="max-width: 70%"
          centered v-model="tab" color="primary" slider-color="accent">
          <v-tab  v-for="(tab, index) in tabs" :key="index">{{ tab.title }}</v-tab>
          <v-tab-item class="mt-10"  v-for="(tab, index) in tabs" :key="index">
            <general-settings v-if="tab.title === 'General settings'"></general-settings>
            <language v-if="tab.title === 'General settings'"></language>
            <v-row class="d-flex justify-center text-center screen-back-color " v-else-if="tab.title === 'Leagues of Legends'">
              <v-card-text class="mt-4">
                You have no linked accounts. Download Blitz to automatically detect your profile.
              </v-card-text>
              <v-card-actions>
                <v-btn class="mb-3" color="error" dark @click="">
                  Download Topal
                </v-btn>
              </v-card-actions>
              <setting-single-project></setting-single-project>
            </v-row>
            <v-row class="d-flex justify-center text-center screen-back-color " v-else-if="tab.title === 'Teamfight Tactics'">
              <v-card-text class="mt-4">
                You have no linked accounts. Download Blitz to automatically detect your profile.
              </v-card-text>
              <v-card-actions>
                <v-btn class="mb-3" color="error" dark @click="">
                  Download Topal
                </v-btn>
              </v-card-actions>
            <settings-teamfight-tactics></settings-teamfight-tactics>
            </v-row>
            <v-row class="d-flex justify-center text-center screen-back-color " v-else-if="tab.title === 'Valorant'">
              <v-card-text class="mt-4">
                You have no linked accounts. Download Blitz to automatically detect your profile.
              </v-card-text>
              <v-card-actions>
                <v-btn class="mb-3" color="error" dark @click="">
                  Download Topal
                </v-btn>
              </v-card-actions>
            </v-row>
            <v-row class="d-flex justify-center text-center screen-back-color " v-else-if="tab.title === 'CS:GO'">
              <v-card-text class="mt-4">
                You have no linked accounts. Download Blitz to automatically detect your profile.
              </v-card-text>
              <v-card-actions>
                <v-btn class="mb-3" color="error" dark @click="">
                  Download Topal
                </v-btn>
              </v-card-actions>
            </v-row>
            <v-row class="d-flex justify-center text-center screen-back-color " v-else-if="tab.title === 'Apex Legends'">
              <v-card-text class="mt-4">
                You have no linked accounts. Download Blitz to automatically detect your profile.
              </v-card-text>
              <v-card-actions>
                <v-btn class="mb-3" color="error" dark @click="">
                  Download Topal
                </v-btn>
              </v-card-actions>
            </v-row>
          </v-tab-item>
        </v-tabs>
      </v-col>
    </div>
  </v-container>
</template>

<script>
import generalSettings from "../components/generalSettings.vue";
import language from "../components/language.vue";
import settingSingleProject from "../components/settingSingleProject.vue";
import settingsTeamfightTactics from "../components/settingsTeamfightTactics.vue";
export default {
  layout: 'detailsPage',
  components:{
    generalSettings,
    language,
    settingSingleProject,
    settingsTeamfightTactics
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
