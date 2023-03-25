<template>
  <v-app>
    <v-container>
      <v-tabs
        centered
        v-model="activeTab" show-arrows>
        <v-tab v-for="tab in tabs" :key="tab.id">{{ tab.label }}</v-tab>
      </v-tabs>
      <v-tabs-items v-model="activeTab">
        <v-tab-item v-for="tab in tabs" :key="tab.id">
          <v-card>
            <v-card-text>
              <h1>{{ tab.title }}</h1>
              <p>{{ tab.content }}</p>
            </v-card-text>
          </v-card>
        </v-tab-item>
      </v-tabs-items>
    </v-container>
  </v-app>
</template>

<script>
export default {
  layout: 'detailsPage',
  data() {
    return {
      activeTab: 0,
      tabs: [
        {
          id: 0,
          label: "All Games",
          title: "All Games",
          content: "Here's the list of all games."
        },
        {
          id: 1,
          label: "Leagues of Legends",
          title: "Leagues of Legends",
          content: "Information about Leagues of Legends."
        },
        {
          id: 2,
          label: "Teamfight Tactics",
          title: "Teamfight Tactics",
          content: "Information about Teamfight Tactics."
        },
        {
          id: 3,
          label: "Valorant",
          title: "Valorant",
          content: "Information about Valorant."
        },
        {
          id: 4,
          label: "CS:GO",
          title: "CS:GO",
          content: "Information about CS:GO."
        },
        {
          id: 5,
          label: "Apex Legends",
          title: "Apex Legends",
          content: "Information about Apex Legends."
        }
      ]
    };
  }
};
</script>


