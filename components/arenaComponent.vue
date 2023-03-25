<template>
  <v-card class="card">
    <v-img :src="imageSource" height="50%" class="card-image"></v-img>
    <v-divider></v-divider>
    <v-row class=" ma-5 mb-0">
      <span class="card-title mr-auto">{{ title }}</span>
      <span class="card-time ml-auto">
        <v-icon class="timer-icon">mdi-timer</v-icon>
        {{ time }}
      </span>
    </v-row>
  </v-card>
</template>

<script>
export default {
  name: 'MyCard',
  props: {
    imageSource: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    time: {
      type: String,
      required: true,
    },
  },
}
</script>

<style scoped>
.card {
  width: 100%;
  height: 250px;
  overflow: hidden;
  border-radius: 5px;
}

.card-image {
  object-fit: cover;
}

.card-title {
  font-size: 24px;
}

.card-time {
  display: flex;
  align-items: center;
  font-size: 18px;
}

.timer-icon {
  margin-right: 8px;
}
</style>
