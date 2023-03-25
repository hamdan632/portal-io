<template>
  <span class="screen-back-color d-flex">
    <v-card-title class="screen-back-color d-flex justify-center" style="margin: 0px!important;">
      <v-card min-height="120" min-width="70">
        <v-card-title class="d-flex justify-center">
          <v-icon
            class="mt-5"
          >mdi-watch</v-icon>
        </v-card-title>
      </v-card>
    </v-card-title>
    <v-card-title class="screen-back-color d-flex justify-center">
      <v-card min-width="250">
        <v-card-title class="ml-5">
          1 Day Event
        </v-card-title>
        <v-card-text class="ml-5">
          Mar 30, 12 AM - Mar 31, 12 AM
        </v-card-text>
      </v-card>
    </v-card-title>
    <v-card-title class="screen-back-color d-flex justify-center">
      <v-card min-width="120">
        <v-card-title class="ml-5">
          3.1k
        </v-card-title>
        <v-card-text class="ml-5">
          Registered
        </v-card-text>
      </v-card>
    </v-card-title>
    <v-card-title class="screen-back-color d-flex justify-center">
      <v-card min-width="120">
        <v-card-title class="ml-5">
          $100
        </v-card-title>
        <v-card-text class="ml-5">
          Prize Pool
        </v-card-text>
      </v-card>
    </v-card-title>
    <v-card-title class="screen-back-color d-flex justify-center">
      <v-card min-height="120" min-width="250">
        <v-card-title>
          <v-btn color="red" class="mt-3 ml-auto mr-auto">
            Sign In To Join
          </v-btn>
        </v-card-title>

      </v-card>
    </v-card-title>
    <v-card-title  class="screen-back-color d-flex justify-center">
      <v-card  min-height="120" min-width="250">
        <v-card-title>
          <v-btn class="mt-3 ml-auto mr-auto">
            More Details
          </v-btn>
        </v-card-title>

      </v-card>
    </v-card-title>
  </span>
</template>

<script>
export default {
  name: 'MyCard',

}
</script>

<style scoped>
.v-card__subtitle, .v-card__text, .v-card__title {
  padding: 16px;
  padding-right: 3px;
  padding-left: 0px;
}
</style>
