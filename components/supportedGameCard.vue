<template>
  <div class="">
    <v-card-title>Supported Games</v-card-title>
    <v-card-title class="d-flex justify-center">
      <v-card-text text @click="goToPage('about-us')">Leagues of Legends</v-card-text>
      <v-card-text text @click="goToPage('partnerships')">Teamfight Tactics</v-card-text>
      <v-card-text text @click="goToPage('careers')">Valorant</v-card-text>
      <v-card-text text @click="goToPage('branding')">CS:GO</v-card-text>
      <v-card-text text @click="goToPage('faq')">Apex Legends</v-card-text>
    </v-card-title>
  </div>
</template>

<script>
export default {
  methods: {
    goToPage(pageName) {
      this.$router.push('/' + pageName);
    }
  }
}
</script>
