<template>
  <v-card>
    <v-card-title class="mt-10">
      General
    </v-card-title>
    <v-card-text>
      <v-row class="d-flex  mt-5">
        <v-row class="d-flex justify-center mr-auto ma-3">
          <div class="subtitle-1">Theme</div>
          <v-btn class="ml-auto  mr-auto" text color="primary" @click="toggleDropdown">
            <v-menu offset-y style="border-radius: 5px" class="screen-back-color">
              <template v-slot:activator="{ on }">
                <v-btn text icon v-on="on">
                  <span>
                    Dark
                  </span>
                  <v-icon>mdi-chevron-down</v-icon>
                </v-btn>
              </template>
              <v-list>
                <v-list-item v-for="(option, index) in dropdownItems" :key="index" @click="">
                  <v-list-item-title>{{ option.title }}</v-list-item-title>
                </v-list-item>
              </v-list>
            </v-menu>
          </v-btn>
        </v-row>
        <v-row class="  d-flex    ml-auto  ">
          <div class="subtitle-1  ml-auto mr-auto">&nbsp;Enable Animations&nbsp;&nbsp;&nbsp;&nbsp;</div>
          <v-switch class="ml-auto  mr-auto mt-0" v-model="surveyEnabled" color="primary"></v-switch>
        </v-row>
      </v-row>
      <v-divider class="mt-3"></v-divider>

      <v-row class="mt-5 d-flex">
        <v-row class="d-flex justify-center mr-auto ma-3 mt-10">
          <div class="subtitle-1  ">Enable Survey </div>
          <v-switch class="ml-auto  mr-auto mt-0" v-model="surveyEnabled" color="primary"></v-switch>
        </v-row>
        <v-row class="  d-flex ml-auto justify-center mb-5  ml-10" >
              <span class="caption ml-auto mb-0 text-break mb-5 mr-auto" style="font-size: 10px !important;">
                <v-card-text>Debug Mood</v-card-text>
                Allows our developers to see what's going on in the app. This is useful <br> for debugging issues, but you should only enable it when <br> asked to do so by a developer.<
            If you're not sure  what this is,
                <br>you should leave it off as it will introduce latency into your games.</span>
            <v-radio class="ml-auto  mr-auto mb-10" value="off" color="primary">Off</v-radio>
        </v-row>
      </v-row>
    </v-card-text>


  </v-card>
</template>

<script>
export default {
  data() {
    return {
      dropdown: false,
      dropdownItems: [
        { title: 'Dark Theme' },
        { title: 'Light Theme' },
        { title: 'Custom Theme' }
      ],
      surveyEnabled: false,
      debugMode: 'off'
    }
  },
  methods: {
    toggleDropdown() {
      this.dropdown = !this.dropdown;
    },
    selectDropdownItem(item) {
      console.log(item);
      // implement logic to select the dropdown item
    }
  }
}
</script>
