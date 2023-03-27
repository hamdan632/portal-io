<template>
  <v-card
    style="background-color: #121212"
    class="ma-3"
    height="420"
    max-width="350"
    @click="$router.push('/gameStats')"
  >
    <v-img
      :elevation="2"
      :transition="{ 'transform': '0.2s ease-out' }"
      class="hoverable-image mr-auto ml-auto mt-1 cursor-pointer"
      src="https://images.unsplash.com/photo-1511512578047-dfb367046420?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80"
      max-width="95%" height="400">
      <v-card-title
        class="mt-10 ml-2 mr-2" style="background-color: #393939; opacity: 0.9; max-height: 80px">
      <span>
        <v-card-text class="d-flex justify-center mt-auto">
          <v-icon class="ma-1">mdi-checkbox-marked-outline</v-icon>
          <span class="mt-1">
                    Hello to the future
          </span>
      </v-card-text>
      </span>
      </v-card-title>
    </v-img>
  </v-card>
</template>
<style scoped>
.hoverable-image:hover {
  transform: scale(1.1);
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.2);
}
</style>
