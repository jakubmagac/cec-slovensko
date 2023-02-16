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

.app {
  color: #0c0c0c;
  background-color: #fff;
}
.layout-container {
  text-align: justify;
  padding: 4em 0;

  @media screen and (max-width: 960px)  {
    padding: 2em 0;
  }
}

footer {
  border-top: 1px solid #0c0c0c;
  background-color: #5b5b5b;
  padding: 2em 0;
  color: #DBDBDB;
}

</style>
