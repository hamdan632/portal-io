<template>
  <v-card class="mx-auto" height="350" width="300">
    <v-img :src="imageSrc" class="ml-2 hoverable-image" height="60%" width="95%"  />
    <v-card-title>{{ cardTitle }}</v-card-title>
    <v-card-text>{{ cardDescription }}</v-card-text>
  </v-card>
</template>

<script>
export default {
  props: {
    imageSrc: {
      type: String,
      required: true
    },

    cardTitle: {
      type: String,
      required: true
    },
    cardDescription: {
      type: String,
      required: true
    },

  }
}
</script>
