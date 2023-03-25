<template>
  <v-card class="" height="300" width="100%">
    <v-row no-gutters>
      <v-col :cols="6" class="mt-10">
        <v-card-title class="ml-5">{{ cardTitle }}</v-card-title>
        <v-card-text>{{ cardDescription }}</v-card-text>
      </v-col>
      <v-col :cols="6">
        <v-img :src="imageSrc" height="100%"  />
      </v-col>
    </v-row>
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
    }
  }
}
</script>
