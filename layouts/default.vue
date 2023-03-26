<template>
  <v-app dark>
    <v-navigation-drawer
      color="black"
      v-model="drawer"
      :mini-variant="right"
      height="100%"
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
      <v-text-field
        class=""
        v-if="showSearchTop"
        light
        dense
        style=" max-height: 30px; max-width: 40%; margin-left: 500px"
        v-model="search"
        :placeholder="searchPlaceholder"
        :solo="solo"
        :clearable="clearable"
        :append-icon="searchIcon"
        @keydown.native.enter="submitSearch"
      ></v-text-field>

      <v-spacer />
      <v-btn
        text
        style="background-color: blue"
        class="mr-2 ml-auto"
        @click="$router.push('/login')"
      >
        <v-icon>mdi-account</v-icon>
        login
      </v-btn>
      <v-btn
        style="background-color: #a90808"
        text
        class="mr-2"
      >
        <v-icon>mdi-arrow-collapse-down</v-icon>
        Download
      </v-btn>
    </v-app-bar>
    <v-main>
      <v-container>
          <v-text-field
            light
            class="ml-auto mr-auto"
            style=" max-height: 60px; max-width: 35%; margin-top: 200px; border-radius: 10px"
            v-if="showSearch"
            v-model="search"
            :placeholder="searchPlaceholder"
            :clearable="clearable"
            :outlined="outlined"
            :solo="solo"
            :append-icon="searchIcon"
            @keydown.native.enter="submitSearch"
          ></v-text-field>
        <Nuxt />
      </v-container>
    </v-main>
    <v-navigation-drawer
      :mini-variant="right"
      v-model="rightDrawer"
      color="black"
      right
      app
      expand-on-hover
      width="250"
    >
      <v-list dense>
        <v-list-item
          class="cursor-pointer"
          @click="">
          <v-list-item-action>
            <v-icon class="" >mdi-account</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-menu offset-y>
              <template v-slot:activator="{ on }" @click.stop="rightDrawer = !rightDrawer">
                  <v-list-item-title class="" v-on="on">Guest Account</v-list-item-title>
              </template>
              <v-list>
                <v-list-item @click="">
                  <v-list-item-icon>
                    <v-icon>mdi-account-plus</v-icon>
                  </v-list-item-icon>
                  <v-list-item-content>
                    <v-list-item-title>Sign Up for Account</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
                <v-list-item @click="">
                  <v-list-item-icon>
                    <v-icon>mdi-translate</v-icon>
                  </v-list-item-icon>
                  <v-list-item-content>
                    <v-list-item-title>Language: English</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
                <v-list-item @click="">
                  <v-list-item-icon>
                    <v-icon>mdi-reload</v-icon>
                  </v-list-item-icon>
                  <v-list-item-content>
                    <v-list-item-title>Reload</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
                <v-list-item @click="">
                  <v-list-item-icon>
                    <v-icon>mdi-shield-lock</v-icon>
                  </v-list-item-icon>
                  <v-list-item-content>
                    <v-list-item-title>Privacy Policy</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
                <v-list-item @click="">
                  <v-list-item-icon>
                    <v-icon>mdi-login</v-icon>
                  </v-list-item-icon>
                  <v-list-item-content>
                    <v-list-item-title>Login</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
              </v-list>
            </v-menu>

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
          class="cursor-pointer"
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
      searchPlaceholder: "Search profiles, champions, agends, legends, and more!",
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
    openRightDrawer(){
      this.rightDrawer = !this.rightDrawer
    },

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
<style>
.img-circle {
  border-radius: 50%;
}
.light-theme {
  background-color: #f5f5f5;
  color: #333;
}

.dark-theme {
  background-color: #111;
  color: #fff;
}
</style>
