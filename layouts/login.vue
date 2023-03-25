<template>
  <v-app dark>
    <v-navigation-drawer
      color="black"
      v-model="drawer"
      :mini-variant="right"
      :clipped="clipped"
      expand-on-hover
      app
    >
      <v-list>
        <v-list-item
          class="d-flex justify-center mt-5 mb-10">
          <v-img
            class="mr-auto"
            height="70"
            max-width="70"
            src="/logo.svg">
          </v-img>
          <v-card-title class="mr-auto">
            Portal IO
          </v-card-title>
        </v-list-item>

        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
      style="background-color: #121212"
    >

      <v-spacer />
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      showSearchTop: false,
      clipped: false,
      drawer: true,
      fixed: false,
      title: "My App",
      color: "primary",
      elevation: 2,
      search: "",
      searchPlaceholder: "Search",
      clearable: true,
      outlined: true,
      rounded: true,
      dense: true,
      solo: true,
      showSearch: true,
      searchIcon: "mdi-magnify",
      items: [
        {
          icon: 'mdi-apps',
          title: 'Home',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Overlays',
          to: '/overlays'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Game Guides',
          to: '/guide'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Arena',
          to: '/arena'
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: true,
    }
  },
  methods: {

    submitSearch() {
      console.log("Search submitted:", this.search);
      // Add your search logic here
    }
  },
  mounted() {
    window.addEventListener("scroll", () => {
      if (window.scrollY > 0) {
        this.elevation = 2;
        this.showSearchTop = true;
      } else {
        this.showSearchTop = false
      }
    });
  }
}
</script>
