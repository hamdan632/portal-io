<template>
  <v-div>
    <v-card-title>Follow Us</v-card-title>
    <v-card-text>
      <v-list>
        <v-list-item v-for="(item, index) in items" :key="index">
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <a :href="item.link">{{ item.text }}</a>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-card-text>
  </v-div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          text: "Facebook",
          icon: "mdi-facebook",
          link: "https://www.facebook.com"
        },
        {
          text: "Twitter",
          icon: "mdi-twitter",
          link: "https://www.twitter.com"
        },
        {
          text: "Instagram",
          icon: "mdi-instagram",
          link: "https://www.instagram.com"
        },
        {
          text: "Our Discord",
          icon: "mdi-discord",
          link: "https://discord.com"
        }
      ]
    };
  }
};
</script>
