<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="right"
      :clipped="clipped"
      expand-on-hover
      app
    >
      <v-img
        height="100"
        width="100"
        src="/v.png">
      </v-img>
      <v-list>
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
      <v-text-field
        dark
        filled
        dense
        color="black"
        style=" max-height: 40px; max-width: 15%;"
        v-model="search"
        :rounded="rounded"
        :placeholder="searchPlaceholder"
        :clearable="clearable"
        :outlined="outlined"
        :solo="solo"
        :append-icon="searchIcon"
        @keydown.native.enter="submitSearch"
      ></v-text-field>

      <v-spacer />
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-navigation-drawer
      :mini-variant="right"
      v-model="drawer"
      right
      app
      expand-on-hover
      width="250"
    >
      <v-list dense>
        <v-list-item
          class="cursor-pointer"
          @click="$router.push('/login')">
          <v-list-item-action>
            <v-icon>mdi-account</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Guest Account</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item
          class="cursor-pointer"
          @click=""
        >
          <v-list-item-action>
            <v-icon>mdi-cloud-download</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Download Top</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item
          class="cursor-pointer"
          @click="$router.push('/settings')"
        >
          <v-list-item-action>
            <v-icon>mdi-account-plus</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Settings</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item
          style="background-color: #5b5b36"
          class="cursor-pointer "
          @click="$router.push('/wallet')"
        >
          <v-list-item-action>
            <v-icon>mdi-account-star</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Get Portal Pro</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item
          class="cursor-pointer"
          @click="$router.push('/login')"
        >
          <v-list-item-action>
            <v-icon>mdi-account-plus</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Sign Up for Account</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item
          class="cursor-pointer"
          @click="$router.push('/wallet')"
        >
          <v-list-item-action>
            <v-icon>mdi-wallet</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            Wallet
          </v-list-item-content>
        </v-list-item>
        <v-divider></v-divider>
        <v-list-item>
          <v-btn class="ml-auto mr-auto mt-2">
            Coming Soon
          </v-btn>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
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
