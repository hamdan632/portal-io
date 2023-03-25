<template>
      <v-container>
          <v-row width="70%" class="d-flex justify-center mt-10 mb-10 after-sticky">
            <div v-for="card in cards" :key="card.id" >
              <game-card :title="card.title" :image-url="card.url">
              </game-card>
            </div>
          </v-row>
        <v-row class="mt-10 ">
          <v-card-title class=" mr-auto ml-auto">
            The Latest:  &nbsp;
            <span class="font-weight-light">
            Take a look at what's new, right now.
          </span>
          </v-card-title>
        </v-row>
        <v-row
          class="d-flex justify-center">
          <div
            style="max-width: 60% !important;"
            v-for="card in latest" :key="card.id"
            class="screen-back-color"
          >
            <latest-card></latest-card>
          </div>

        </v-row>
        <v-row
          class="d-flex justify-center">
          <div
            style="max-width: 60% !important;"
            v-for="card in latest" :key="card.id"
            class="screen-back-color"
          >
            <latest-card></latest-card>
          </div>

        </v-row>
        <div class="d-flex ml-auto mr-auto">
          <v-card-title class="ml-auto mr-auto mt-10">
            Your Personal Gaming Coach
          </v-card-title>
        </div>
        <span class="d-flex justify-center text-center">
          <v-card-text class="mr-auto ml-auto">
            Portal simplifies the process of mastering difficult games,
            helping you improve at every step of your journey to the top.
          </v-card-text>
        </span>
        <v-card class="mt-10">
          <v-row >
            <v-col>
              <card class="d-flex justify-center ml-auto mr-auto">
                <div>
                  <v-img
                    height="80"
                    width="80"
                    src="/company-log.svg"
                  >
                  </v-img>
                  <v-card-title>
                    PORTAL IO
                  </v-card-title>
                  <v-btn color="green">
                    Complaint Us
                  </v-btn>
                </div>
              </card>
            </v-col>
            <v-col>
              <footer-section ></footer-section>
            </v-col>
            <v-col>
              <supported-game-card></supported-game-card>
            </v-col>
            <v-col>
              <footer-section-socials></footer-section-socials>
            </v-col>
          </v-row>
        </v-card>
        </v-container>
</template>

<script>
import GameCard from "../components/gameCard.vue";
import latestCard from "../components/latestCard.vue";
import footerSection from "../components/footerSection.vue";
import FooterSectionSocials from "../components/footerSectionSocials.vue";
import supportedGameCard from "../components/supportedGameCard.vue";
export default {
  components: {
    FooterSectionSocials,
    GameCard,
    latestCard,
    footerSection,
    supportedGameCard
  },
  data() {
    return {
      search: '',
      cards: [
        { id: 1, title: 'Leagues of Legends', url: 'https://images.unsplash.com/photo-1553481187-be93c21490a9?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80' },
        { id: 2, title: 'TeamFight Tactics', url: 'https://images.unsplash.com/photo-1511512578047-dfb367046420?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80' },
        { id: 3, title: 'Valorant', url: 'https://images.unsplash.com/photo-1519669556878-63bdad8a1a49?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80' },
        { id: 4, title: 'CS:GO', url: 'https://images.unsplash.com/photo-1586165368502-1bad197a6461?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1258&q=80' },
        { id: 5, title: 'Apex Legends', url: 'https://images.unsplash.com/photo-1614285457768-646f65ca8548?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80' },
      ],
      latest: [
        { id: 1, title: 'Leagues of Legends', url: 'https://images.unsplash.com/photo-1553481187-be93c21490a9?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80' },
        { id: 2, title: 'TeamFight Tactics', url: 'https://images.unsplash.com/photo-1511512578047-dfb367046420?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80' },
        { id: 3, title: 'Valorant', url: 'https://images.unsplash.com/photo-1519669556878-63bdad8a1a49?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80' },
      ]
    }
  }
}
</script>
<style scoped>
.search-field {
  width: 100%;
  padding: 16px;
}
.sticky-card {
  width: 344px;
  position: fixed;
  top: 10%;
  margin-bottom: auto;
  z-index: 1;
  /* centering */
  left: 50%;
  transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  -webkit-transform: translate(-50%, -50%);
}

.after-sticky {
  margin-top: 90px;
}
</style>
