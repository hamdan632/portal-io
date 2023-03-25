<template>
  <v-card class="ma-3">
    <v-card-title class="ml-2">
      <v-icon>{{ icon }}</v-icon>
    </v-card-title>
    <v-card-title class="ml-2">{{ title }}</v-card-title>

    <v-card-text>{{ description }}</v-card-text>
  </v-card>
</template>

<script>
export default {
  props: {
    icon: {
      type: String,
      required: true
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
