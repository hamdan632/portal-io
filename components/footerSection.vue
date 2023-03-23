<template>
  <div class="">
    <v-card-title>Company</v-card-title>
    <v-card-title class="d-flex justify-center">
      <v-card-text text @click="goToPage('about-us')">About Us</v-card-text>
      <v-card-text text @click="goToPage('partnerships')">Partnerships</v-card-text>
      <v-card-text text @click="goToPage('careers')">Careers</v-card-text>
      <v-card-text text @click="goToPage('branding')">Branding</v-card-text>
      <v-card-text text @click="goToPage('faq')">FAQ</v-card-text>
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
