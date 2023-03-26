<template>
  <v-card class="my-card" height="200">
    <v-row>
      <v-col cols="3" height="100%">
        <v-img style="height: 200px" src="background-game.jpg" ></v-img>
      </v-col>
      <v-col cols="9">
        <v-card-title class="">{{ title }}</v-card-title>
        <v-card-title class="font-weight-light font-weight-thin">{{ description }}</v-card-title>
        <v-card-title>
          <v-btn class="" :class="{ 'green--text': isEnabled, 'red--text': !isEnabled }" @click="toggleEnable">
            {{ isEnabled ? 'Disable' : 'Enable' }}
          </v-btn>
        </v-card-title>
      </v-col>

    </v-row>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      isEnabled: true,
      title: 'Use skin artwork for champion portraits',
      description: 'Use TFT set skin artwork when displaying/representing champion images.'
    }
  },
  methods: {
    toggleEnable() {
      this.isEnabled = !this.isEnabled
    }
  }
}
</script>

<style>
.my-card {
  width: 100%;
}
.title {
  align-self: flex-start;
}
.description {
  align-self: center;
  margin-top: 10px;
  margin-bottom: 10px;
}
</style>
