<template>
  <v-app>
    <header>
      <v-navigation-drawer
        v-model="sidebar"
        disable-resize-watcher
        class="hidden-md-and-up"
        style="background-color: #0c0c0c"
        app
      >
        <div
          v-for="item in menuItems"
          :key="item.title"
          class="drawer-button"
        >
          <a
            :href="item.path"
            class="menu-link"
          >
            <div>
              {{ item.title }}
            </div>
          </a>
        </div>
      </v-navigation-drawer>

      <v-app-bar color="#0c0c0c" app>
        <v-img
          lazy-src="/logo.png"
          src="/logo.png"
          max-height="50"
          max-width="200"
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
            :style="$vuetify.breakpoint.mdAndDown ? 'font-size: 0.6rem' : '1rem'"
            text
          >
            {{ item.title }}
          </v-btn>
        </v-toolbar-items>
      </v-app-bar>
    </header>
    <main class="app">
      <Nuxt />
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
      fixed: false,
      miniVariant: false,
      sidebar: false,
      menuItems: [
        { title: 'Home', path: '/' },
        { title: 'Register', path: '/register' },
        { title: 'Location', path: '/location' },
        { title: 'Schedule', path: '/schedule' },
        { title: 'Workshops', path: '/workshops' },
        { title: 'Contact us', path: '/contact' },
        { title: 'Terms & Conditions', path: '/terms-conditions' }
      ]
    }
  },
  methods: {
  }
}
</script>

<style lang="scss">
.v-application {
  font-family: 'Poppins';
  font-weight: 300;
}

.v-application--wrap {
  justify-content: space-between;
  background-color: #fff;
}

.drawer-button {
  padding: 1em 0;
}

.menu-link {
  text-decoration: none;
  text-align: center;
  padding: 2em 0;
  color: white !important;
  cursor: pointer;
}

.menu-link:hover {
  color: #D91D5D !important;
  background-color: #0c0c0cb0;
}

.app {
  color: #0c0c0c;
  background-color: #fff;
}

footer {
  background-color: #0B3D59;
  padding: 2em 0;
  color: #DBDBDB;
}

</style>
