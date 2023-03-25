<template>
  <v-card :style="{ height: height + 'px', width: width + 'px' }" class="ma-2">
    <v-img src="background-game.jpg" max-height="95%"  class="mt-1 hoverable-image" >
      <v-icon class="ma-2 ml-10">mdi-group</v-icon>
      <v-card-title>
        {{ title }}
      </v-card-title>
      <v-card-text>{{ description }}</v-card-text>
    </v-img>

  </v-card>
</template>

<script>
export default {
  props: {
    height: {
      type: Number,
      default: 150
    },
    width: {
      type: Number,
      default: 400
    },

    title: {
      type: String,
      required: true
    },
    description: {
      type: String,
      required: true
    }
  }
}
</script>
<style scoped>
.hoverable-image:hover {
  transform: scale(1.1);
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.2);
}
</style>
