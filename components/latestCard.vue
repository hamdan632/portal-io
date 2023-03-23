<template>
  <v-card
    style="background-color: #121212"
    class="ma-3"
    height="405"
    max-width="305"
  >
    <v-img
      :elevation="2"
      :transition="{ 'transform': '0.2s ease-out' }"
      class="hoverable-image mr-auto ml-auto mt-1 cursor-pointer"
      src="https://images.unsplash.com/photo-1511512578047-dfb367046420?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80"
      max-width="300" height="400">
      <div >
      <span>
        <v-card-title class="d-flex justify-center mt-auto">
        Hello to the future
      </v-card-title>
      </span>
      </div>
    </v-img>
  </v-card>
</template>
<style scoped>
.hoverable-image:hover {
  transform: scale(1.1);
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.2);
}
</style>
