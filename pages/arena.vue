<template>
  <v-container class="">
    <div style="margin-left: 10%;">
      <v-col >
        <v-card-title>Topal's Arenas</v-card-title>
        <v-tabs
          style="max-width: 70%"
          centered v-model="tab" color="primary" slider-color="accent">
          <v-tab
            v-for="(tab, index) in tabs" :key="index">{{ tab.title }}</v-tab>
          <v-tab-item v-for="(tab, index) in tabs" :key="index" style="background-color: #121212">
            <v-card v-if="tab.title === 'All Games'" style="background-color: #121212">
              <v-row class="screen-back-color mt-5" style="background-color: #121212">
                <arena-component title="ARAM Cup 2" time="Starts in: 03d 22h 09m" image-source="https://images.unsplash.com/photo-1508098682722-e99c43a406b2?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80"></arena-component>
              </v-row>
              <arena-stats-component></arena-stats-component>
              <v-card-title>
                Browse Events
              </v-card-title>
              <v-divider></v-divider>
              <arena-table></arena-table>
              <v-card-title class="d-flex justify-center">
                <v-card-title class="text-center">
                  How does Blitz Arena work?
                </v-card-title>
                <v-card-text class="text-center">
                  You don't have to be a professional gamer to join esports tournaments!
                </v-card-text>
              </v-card-title>
              <v-row>
                <arena-guide
                  card-description="Sign up above and practice while you wait."
                  card-title="1.Register!"
                  image-src="https://plus.unsplash.com/premium_photo-1679086008607-8a422e583aa4?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=784&q=80"></arena-guide>
                <arena-guide card-description="Complete mission objectives to score points and climb the leaderboard." card-title="2. Play games!" image-src="https://images.unsplash.com/photo-1542751371-adc38448a05e?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80"></arena-guide>
                <arena-guide card-description="Win everything from cash to gaming PCs and gift cards!" card-title="3. Win prizes!" image-src="https://images.unsplash.com/photo-1618255342875-a1d288c04939?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80"></arena-guide>
              </v-row>
              <v-row class="d-flex justify-center text-center mt-10">
                <arena-bottom-card
                  card-description="Blitz Arena events happen on a regular basis. Check back often to join fun events with exciting partners, challenging missions, and great prizes!"
                  card-title="Join events to climb and shine!"
                  image-src="https://images.unsplash.com/photo-1678145023183-59b5f23e50d4?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80">
                </arena-bottom-card>
              </v-row>
        </v-card>

            <v-card v-if="tab.title === 'Leagues of Legends'">
              <v-row class="screen-back-color mt-5" style="background-color: #121212">
                <arena-component title="ARAM Cup 2" time="Starts in: 03d 22h 09m" image-source="https://images.unsplash.com/photo-1508098682722-e99c43a406b2?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80"></arena-component>
              </v-row>
              <arena-stats-component></arena-stats-component>
              <v-card-title>
                Browse Events
              </v-card-title>
              <v-divider></v-divider>
              <arena-table></arena-table>
              <v-card-title class="d-flex justify-center">
                <v-card-title class="text-center">
                  How does Blitz Arena work?
                </v-card-title>
                <v-card-text class="text-center">
                  You don't have to be a professional gamer to join esports tournaments!
                </v-card-text>
              </v-card-title>
              <v-row>
                <arena-guide
                  card-description="Sign up above and practice while you wait."
                  card-title="1.Register!"
                  image-src="https://plus.unsplash.com/premium_photo-1679086008607-8a422e583aa4?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=784&q=80"></arena-guide>
                <arena-guide card-description="Complete mission objectives to score points and climb the leaderboard." card-title="2. Play games!" image-src="https://images.unsplash.com/photo-1542751371-adc38448a05e?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80"></arena-guide>
                <arena-guide card-description="Win everything from cash to gaming PCs and gift cards!" card-title="3. Win prizes!" image-src="https://images.unsplash.com/photo-1618255342875-a1d288c04939?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80"></arena-guide>
              </v-row>
              <v-row class="d-flex justify-center text-center mt-10">
                <arena-bottom-card
                  card-description="Blitz Arena events happen on a regular basis. Check back often to join fun events with exciting partners, challenging missions, and great prizes!"
                  card-title="Join events to climb and shine!"
                  image-src="https://images.unsplash.com/photo-1678145023183-59b5f23e50d4?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80">
                </arena-bottom-card>
              </v-row>
            </v-card>
            <v-card v-if="tab.title === 'Teamfight Tactics'">
              <v-row class="screen-back-color mt-5" style="background-color: #121212">
                <arena-component title="ARAM Cup 2" time="Starts in: 03d 22h 09m" image-source="https://images.unsplash.com/photo-1508098682722-e99c43a406b2?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80"></arena-component>
              </v-row>
              <v-card-title class="mt-5">
                Browse Events
              </v-card-title>
              <v-divider></v-divider>
              <arena-table></arena-table>
              <v-card-title class="d-flex justify-center">
                <v-card-title class="text-center">
                  How does Blitz Arena work?
                </v-card-title>
                <v-card-text class="text-center">
                  You don't have to be a professional gamer to join esports tournaments!
                </v-card-text>
              </v-card-title>
              <v-row>
                <arena-guide
                  card-description="Sign up above and practice while you wait."
                  card-title="1.Register!"
                  image-src="https://plus.unsplash.com/premium_photo-1679086008607-8a422e583aa4?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=784&q=80"></arena-guide>
                <arena-guide card-description="Complete mission objectives to score points and climb the leaderboard." card-title="2. Play games!" image-src="https://images.unsplash.com/photo-1542751371-adc38448a05e?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80"></arena-guide>
                <arena-guide card-description="Win everything from cash to gaming PCs and gift cards!" card-title="3. Win prizes!" image-src="https://images.unsplash.com/photo-1618255342875-a1d288c04939?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80"></arena-guide>
              </v-row>
              <v-row class="d-flex justify-center text-center mt-10">
                <arena-bottom-card
                  card-description="Blitz Arena events happen on a regular basis. Check back often to join fun events with exciting partners, challenging missions, and great prizes!"
                  card-title="Join events to climb and shine!"
                  image-src="https://images.unsplash.com/photo-1678145023183-59b5f23e50d4?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80">
                </arena-bottom-card>
              </v-row>
            </v-card>
            <v-card v-if="tab.title === 'Valorant'">
              <v-row class="screen-back-color mt-5" style="background-color: #121212">
                <arena-component title="ARAM Cup 2" time="Starts in: 03d 22h 09m" image-source="https://images.unsplash.com/photo-1508098682722-e99c43a406b2?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80"></arena-component>
              </v-row>
              <v-card-title class="mt-5">
                Browse Events
              </v-card-title>
              <v-divider></v-divider>
              <arena-table></arena-table>
              <v-card-title class="d-flex justify-center">
                <v-card-title class="text-center">
                  How does Blitz Arena work?
                </v-card-title>
                <v-card-text class="text-center">
                  You don't have to be a professional gamer to join esports tournaments!
                </v-card-text>
              </v-card-title>
              <v-row>
                <arena-guide
                  card-description="Sign up above and practice while you wait."
                  card-title="1.Register!"
                  image-src="https://plus.unsplash.com/premium_photo-1679086008607-8a422e583aa4?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=784&q=80"></arena-guide>
                <arena-guide card-description="Complete mission objectives to score points and climb the leaderboard." card-title="2. Play games!" image-src="https://images.unsplash.com/photo-1542751371-adc38448a05e?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80"></arena-guide>
                <arena-guide card-description="Win everything from cash to gaming PCs and gift cards!" card-title="3. Win prizes!" image-src="https://images.unsplash.com/photo-1618255342875-a1d288c04939?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80"></arena-guide>
              </v-row>
              <v-row class="d-flex justify-center text-center mt-10">
                <arena-bottom-card
                  card-description="Blitz Arena events happen on a regular basis. Check back often to join fun events with exciting partners, challenging missions, and great prizes!"
                  card-title="Join events to climb and shine!"
                  image-src="https://images.unsplash.com/photo-1678145023183-59b5f23e50d4?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80">
                </arena-bottom-card>
              </v-row>
            </v-card>
            <v-card v-if="tab.title === 'CS:GO'">
              <v-row class="screen-back-color mt-5" style="background-color: #121212">
                <arena-component title="" time="" image-source="https://images.unsplash.com/photo-1508098682722-e99c43a406b2?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80"></arena-component>
              </v-row>
              <v-card-title class="mt-5">
                Browse Events
              </v-card-title>
              <v-divider></v-divider>
              <arena-table></arena-table>
              <v-card-title class="d-flex justify-center">
                <v-card-title class="text-center">
                  How does Blitz Arena work?
                </v-card-title>
                <v-card-text class="text-center">
                  You don't have to be a professional gamer to join esports tournaments!
                </v-card-text>
              </v-card-title>
              <v-row>
                <arena-guide
                  card-description="Sign up above and practice while you wait."
                  card-title="1.Register!"
                  image-src="https://plus.unsplash.com/premium_photo-1679086008607-8a422e583aa4?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=784&q=80"></arena-guide>
                <arena-guide card-description="Complete mission objectives to score points and climb the leaderboard." card-title="2. Play games!" image-src="https://images.unsplash.com/photo-1542751371-adc38448a05e?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80"></arena-guide>
                <arena-guide card-description="Win everything from cash to gaming PCs and gift cards!" card-title="3. Win prizes!" image-src="https://images.unsplash.com/photo-1618255342875-a1d288c04939?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80"></arena-guide>
              </v-row>
              <v-row class="d-flex justify-center text-center mt-10">
                <arena-bottom-card
                  card-description="Blitz Arena events happen on a regular basis. Check back often to join fun events with exciting partners, challenging missions, and great prizes!"
                  card-title="Join events to climb and shine!"
                  image-src="https://images.unsplash.com/photo-1678145023183-59b5f23e50d4?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80">
                </arena-bottom-card>
              </v-row>
            </v-card>
            <v-card v-if="tab.title === 'Apex Legends'">
              <v-row class="screen-back-color mt-5" style="background-color: #121212">
                <arena-component title="ARAM Cup 2" time="Starts in: 03d 22h 09m" image-source="https://images.unsplash.com/photo-1508098682722-e99c43a406b2?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80"></arena-component>
              </v-row>
              <v-card-title class="mt-5">
                Browse Events
              </v-card-title>
              <v-divider></v-divider>
              <arena-table></arena-table>
              <v-card-title class="d-flex justify-center">
                <v-card-title class="text-center">
                  How does Blitz Arena work?
                </v-card-title>
                <v-card-text class="text-center">
                  You don't have to be a professional gamer to join esports tournaments!
                </v-card-text>
              </v-card-title>
              <v-row>
                <arena-guide
                  card-description="Sign up above and practice while you wait."
                  card-title="1.Register!"
                  image-src="https://plus.unsplash.com/premium_photo-1679086008607-8a422e583aa4?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=784&q=80"></arena-guide>
                <arena-guide card-description="Complete mission objectives to score points and climb the leaderboard." card-title="2. Play games!" image-src="https://images.unsplash.com/photo-1542751371-adc38448a05e?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80"></arena-guide>
                <arena-guide card-description="Win everything from cash to gaming PCs and gift cards!" card-title="3. Win prizes!" image-src="https://images.unsplash.com/photo-1618255342875-a1d288c04939?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80"></arena-guide>
              </v-row>
              <v-row class="d-flex justify-center text-center mt-10">
                <arena-bottom-card
                  card-description="Blitz Arena events happen on a regular basis. Check back often to join fun events with exciting partners, challenging missions, and great prizes!"
                  card-title="Join events to climb and shine!"
                  image-src="https://images.unsplash.com/photo-1678145023183-59b5f23e50d4?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80">
                </arena-bottom-card>
              </v-row>
            </v-card>


          </v-tab-item>
        </v-tabs>
      </v-col>
    </div>
  </v-container>
</template>

<script>
import arenaComponent from "../components/arenaComponent.vue";
import gameGuideComponent from "../components/gameGuideComponent.vue";
import gameGuideChildImageComponent from "../components/gameGuideChildImageComponent.vue";
import arenaStatsComponent from "../components/arenaStatsComponent.vue";
import arenaTable from "../components/arenaTable.vue";
import arenaGuide from "../components/arenaGuide.vue";
import arenaBottomCard from "../components/arenaBottomCard.vue";
export default {
  layout: 'detailsPage',
  components:{
    gameGuideComponent,
    gameGuideChildImageComponent,
    arenaComponent,
    arenaStatsComponent,
    arenaTable,
    arenaGuide,
    arenaBottomCard
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
