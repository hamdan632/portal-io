<template>
  <v-card class="card d-flex justify-center ma-3" height="300" width="250">
    <!-- Image with settings icon -->
    <v-img
      class="ma-1 hoverable-image ml-auto"
      :src="randomcity" height="50%" width="100%">
      <v-btn icon left class="settings-btn">
        <v-icon>mdi-cog-outline</v-icon>
      </v-btn>
    </v-img>

    <!-- Title and switch button -->
    <v-row align="center" class="title-row" height="50%">
      <v-col cols="8">
        <v-subheader>Title Here</v-subheader>
      </v-col>
      <v-col cols="4">
        <v-switch v-model="switchValue" color="primary"></v-switch>
      </v-col>
    </v-row>

    <!-- Small text with light background -->
    <v-row class="ml-2 ma-1">
       <span class="small-text mr-2" color="white lighten-4" style="background-color: grey">
      New
    </span>
      <span class="small-text mr-2" color="white lighten-4" style="background-color: grey">
      Tracker
    </span>
    </v-row>


    <!-- Description -->
    <v-card-text class="description">
      Description goes here.
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      switchValue: false,
      randomURL: [
        "https://images.unsplash.com/photo-1631896928983-2c94ea6f97e8?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80",
        "https://images.unsplash.com/photo-1496483353456-90997957cf99?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=685&q=80",
        "https://images.unsplash.com/photo-1493217465235-252dd9c0d632?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80",
        "https://images.unsplash.com/photo-1496715976403-7e36dc43f17b?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80",
        "https://images.unsplash.com/photo-1633422424846-f4fbdb443613?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80",
        "https://images.unsplash.com/photo-1434648957308-5e6a859697e8?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1074&q=80",
        "https://images.unsplash.com/photo-1500705077387-65f31ef00c90?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1154&q=80",
        "https://images.unsplash.com/photo-1577179269308-b2e290d07ce5?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80",
        "https://images.unsplash.com/photo-1611162617213-7d7a39e9b1d7?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1074&q=80",
        "https://images.unsplash.com/photo-1611606063065-ee7946f0787a?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1074&q=80"],
    };
  },
  computed: {
    randomcity () {
      return this.randomURL[Math.floor(Math.random()*this.randomURL.length)]
    }
  },
  methods:{
    getRandomURL () {
      return this.randomURL[Math.floor(Math.random()*this.randomURL.length)]
    }
  }
};
</script>

<style>
.card {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding: 16px;
}

.settings-btn {
  color: white;
}

.title-row {
  font-weight: bold;
}

.small-text {
  font-size: 12px;
  padding: 8px;
}

.description {
  font-size: 12px;
}
</style>
