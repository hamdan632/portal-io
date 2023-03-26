<template>
  <v-card class="pa-2" style="background-color: #090707">
    <v-card-title class="ml-3 mt-5">Game Settings</v-card-title>
    <v-container>
      <v-row>
        <v-col class="" cols="12" md="6" v-for="(section, index) in sections" :key="index">
          <v-row style="max-height: 200px">
            <v-col max-height="200">
              <v-card-title class="">{{ section.title }}</v-card-title>
              <v-card-text>{{ section.description }}</v-card-text>
            </v-col>
            <v-card-actions>
              <v-row v-if="section.title === 'Default Flash placement'">
                <v-btn text>Left</v-btn>
                <v-btn text>Right</v-btn>
              </v-row>
              <v-radio v-else v-model="section.selectedOption"  ></v-radio>
            </v-card-actions>
          </v-row>
            <v-divider></v-divider>
        </v-col>
      </v-row>
    </v-container>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      tab: 0,
      sections: [
        {
          title: 'Automatically pop up during champion',
          description: 'Once you’ve locked in a Champion, Blitz will automatically pop up to display builds you can import and other helpful info.',
          selectedOption: '',
          options: [
            { label: 'Option 1', value: 'option1' },
            { label: 'Option 2', value: 'option2' },
            { label: 'Option 3', value: 'option3' },
          ],
        },
        {
          title: 'Enable Match Found Popup',
          description: 'A popup that gives you the option to Accept or Decline when a match has been found (LOL & TFT only).',
          selectedOption: '',
          options: [
            { label: 'Option 1', value: 'option1' },
            { label: 'Option 2', value: 'option2' },
            { label: 'Option 3', value: 'option3' },
          ],
        },
        {
          title: 'Auto import runes',
          description: 'Set runes automatically when entering champion select.',
          selectedOption: '',
          options: [
            { label: 'Option 1', value: 'option1' },
            { label: 'Option 2', value: 'option2' },
            { label: 'Option 3', value: 'option3' },
          ],
        },
        {
          title: 'Auto import summoner spells',
          description: 'Set summoner spells automatically when entering champion select.',
          selectedOption: '',
          options: [
            { label: 'Option 1', value: 'option1' },
            { label: 'Option 2', value: 'option2' },
            { label: 'Option 3', value: 'option3' },
          ],
        },
        {
          title: 'Tilt-free mode',
          description: 'Hide all player ranks and info in champion select.',
          selectedOption: '',
          options: [
            { label: 'Option 1', value: 'option1' },
            { label: 'Option 2', value: 'option2' },
            { label: 'Option 3', value: 'option3' },
          ],
        },
        {
          title: 'Auto import builds',
          description: 'Import matchup and pro item builds into the in-game item shop.',
          selectedOption: '',
          options: [
            { label: 'Option 1', value: 'option1' },
            { label: 'Option 2', value: 'option2' },
            { label: 'Option 3', value: 'option3' },
          ],
        },
        {
          title: 'Default Flash placement',
          description: 'Set the preferred placement of Flash when summoner spells are imported.',
          selectedOption: '',
          options: [
            { label: 'Option 1', value: 'option1' },
            { label: 'Option 2', value: 'option2' },
            { label: 'Option 3', value: 'option3' },
          ],
        },
      ],
    };
  },
};
</script>
