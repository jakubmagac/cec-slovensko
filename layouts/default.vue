<template>
  <v-app>
    <header>
      <v-navigation-drawer
        v-model="sidebar"
        class="hidden-md-and-up"
        app
      >
        <a
          v-for="item in menuItems"
          :key="item.title"
          :href="item.path"
        >
          <div>
            {{ item.title }}
          </div>
        </a>
      </v-navigation-drawer>

      <v-app-bar color="black" app>
        <v-img
          lazy-src="/logo.png"
          src="/logo.png"
          max-height="75"
          min-height="75"
          max-width="75"
          min-width="75"
        />
        <v-spacer />
        <span class="hidden-md-and-up">
          <v-icon color="white" @click="sidebar = !sidebar">mdi-menu</v-icon>
        </span>
        <v-toolbar-items class="hidden-sm-and-down">
          <v-btn
            v-for="item in menuItems"
            :key="item.title"
            :to="item.path"
            style="color: white;"
            text
          >
            {{ item.title }}
          </v-btn>
        </v-toolbar-items>
      </v-app-bar>
    </header>
    <main class="app">
      <v-container>
        <v-row justify="center">
          <v-col cols="8">
            <div ref="content" class="layout-container">
              <Nuxt />
            </div>
          </v-col>
        </v-row>
      </v-container>
    </main>
    <footer class="text-center">
      <div class="d-flex justify-center mb-4">
        <v-icon color="white" class="mr-4">mdi-facebook</v-icon>
        <v-icon color="white">mdi-instagram</v-icon>
      </div>
      <span>&copy; {{ new Date().getFullYear() }} 46th Central European Convention</span>
    </footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js',
      animation: false,
      sidebar: false,
      menuItems: [
        { title: 'Home', path: '/' },
        { title: 'Register', path: '/register' },
        { title: 'Location', path: '/location' },
        { title: 'Schedule', path: '/schedule' },
        { title: 'Workshops', path: '/workshops' },
        { title: 'Contat us', path: '/contact' }
      ]
    }
  },
  methods: {
  }
}
</script>

<style lang="scss">
.app {
  color: #0c0c0c;
  background-color: #f2f2f2;
}
.layout-container {
  text-align: justify;
  padding: 4em 0;

  @media screen and (max-width: 960px)  {
    padding: 2em 0;
  }
}

footer {
  background-color: #5b5b5b;
  padding: 2em 0;
  color: #DBDBDB;
}

</style>
