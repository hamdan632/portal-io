<template>
  <v-card>
    <v-card-title class="mt-5">
      General
    </v-card-title>
    <v-card-text>
      <v-row class="d-flex ">
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
        <v-row class=" d-flex  ">
          <div class="ml-auto mr-16">Enable Animations</div>
          <v-switch class="ml-auto  mr-auto" v-model="surveyEnabled" color="primary"></v-switch>
        </v-row>
      </v-row>
      <v-divider class="mt-2"></v-divider>

      <v-row class="mt-1 d-flex">
        <v-row class="d-flex justify-center mr-auto ma-3 mt-10">
          <div class="  ">Enable Survey </div>
          <v-switch class="ml-auto  mr-auto mt-0" v-model="surveyEnabled" color="primary"></v-switch>
        </v-row>
        <v-row class="  d-flex  justify-center " >
              <span class=" ml-auto mb-0 text-break mb-5 " style="font-size: 10px !important; margin-right: 10px">
                <v-card-text>Debug Mood</v-card-text>
                Allows our developers to see  what's going on in the app. <br> This is useful for debugging issues, <br> but you should only <br> enable it when  asked to do so by a developer</span>
            <v-radio class="mr-auto ml-auto mb-5" value="off" color="primary">Off</v-radio>
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
