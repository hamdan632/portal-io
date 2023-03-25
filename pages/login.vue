<template>
  <v-app>
    <v-main>
      <v-container fluid fill-height>
        <v-row justify="center" align="center" >
          <v-col cols="12" class="text-center">
            <!-- Replace logo with your own logo image source -->
          </v-col>
          <v-col cols="12" class="text-center">
            <v-img src="/logo.svg" width="200" height="200" @click="playAnimation" class="animated-logo ml-auto mr-auto mb-5"></v-img>

            <h1 class="display-1">Welcome to Topal</h1>
          </v-col>
          <v-col cols="12" md="6" lg="4">
            <v-form max-width="100">
              <v-text-field  label="Email" v-model="email" required></v-text-field>
            </v-form>
          </v-col>
          <v-col cols="12" class="text-center">
            <p>Don't have an account? <v-btn text @click="register">Register</v-btn></p>
          </v-col>
          <v-col cols="12" class="text-center">
            <v-btn color="primary" @click="login">Guest Account</v-btn>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  layout: 'login',
  data() {
    return {
      logo: "/logo.gif", // Replace with your own logo image source
      email: ""
    };
  },
  methods: {
    playAnimation() {
      // Play your logo animation here
    },
    login() {
      // Implement login functionality here
    },
    register() {
      // Implement register functionality here
    }
  }
};
</script>

<style scoped>
.animated-logo {
  animation: logo-animation 1s infinite;
}

@keyframes logo-animation {
  0% {
    transform: rotate(0);
  }
  100% {
    transform: rotate(360deg);
  }
}
</style>
