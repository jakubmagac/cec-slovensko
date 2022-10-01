<template>
  <v-app>
    <v-navigation-drawer
      v-if="drawer && $vuetify.breakpoint.smAndDown"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
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
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <header
      style="background: url('./poster.jpg'); background-attachment: fixed; min-height: 100vh; background-size: cover; display: flex; align-items: flex-start;"
    >
      <div style="background-color: #000000A0; width: 100%; height: 100%; ">
        <v-container fluid style="position: relative; z-index: 2; height: 100%;">
          <v-row>
            <v-col cols="2">
              <v-img
                lazy-src="/logo.png"
                src="/logo.png"
                max-height="200"
                max-width="200"
              />
            </v-col>
            <v-spacer />
            <v-col cols="8" style="display: flex; align-items: center;">
              <v-app-bar-nav-icon v-if="$vuetify.breakpoint.smAndDown" @click.stop="drawer = !drawer" />
              <ul class="d-flex menu">
                <li>
                  <NuxtLink to="/">
                    Home
                  </NuxtLink>
                </li>
                <li>
                  <NuxtLink to="/registration">
                    Registration
                  </NuxtLink>
                </li>
                <li>
                  <NuxtLink to="/location">
                    Location
                  </NuxtLink>
                </li>
                <li>
                  <NuxtLink to="/schedule">
                    Schedule
                  </NuxtLink>
                </li>
                <li>
                  <NuxtLink to="/workshops">
                    Workshops
                  </NuxtLink>
                </li>
              </ul>
            </v-col>
          </v-row>
          <v-row style="position: relative; top: 100px;">
            <v-col class="text-center">
              <h1 style="color: #fff; font-weight: 400; font-size: 4rem;" :style="animation ? '' : 'visibility: hidden;'" class="ml2" v-html="header" />
              <template v-if="$nuxt.$route.name === 'index'">
                <h2 style="color: #fff; font-weight: 400; font-size: 1.3rem;" class="mt-4 mb-8">19th - 21th of May 2022</h2>
              </template>
              <v-icon x-large color="white" class="arrow-animation" @click="scroll">mdi-chevron-down</v-icon>
            </v-col>
          </v-row>
        </v-container>
      </div>
    </header>
    <main>
      <div ref="content" class="layout-container">
        <Nuxt />
      </div>
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
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js',
      animation: false
    }
  },
  computed: {
    header () {
      if (this.$nuxt.$route.name === 'index') {
        return '46th Central European Convention'
      }
      if (this.$nuxt.$route.name === 'registration') {
        return 'Registration'
      }
      if (this.$nuxt.$route.name === 'location') {
        return 'Location'
      }
      if (this.$nuxt.$route.name === 'schedule') {
        return 'Schedule'
      }
      if (this.$nuxt.$route.name === 'workshops') {
        return 'Workshops'
      }
      return ''
    }
  },
  mounted () {
    const textWrapper = document.querySelector('.ml2')
    textWrapper.innerHTML = textWrapper.textContent.replace(/\S/g, "<span class='letter'>$&</span>")

    this.animation = true
    this.$anime.timeline({ loop: false })
      .add({
        targets: '.ml2 .letter',
        scale: [4, 1],
        opacity: [0, 1],
        translateZ: 0,
        easing: 'easeOutExpo',
        duration: 850,
        delay: (el, i) => 70 * i
      })
  },
  methods: {
    scroll () {
      this.$refs.content.scrollIntoView({ behavior: 'smooth', block: 'start', inline: 'nearest' })
    }
  }
}
</script>

<style lang="scss">
.layout-container {
  font-size: 1.5rem;
}

.menu {
  list-style: none; width: 100%; color: white; justify-content: space-around;
  font-size: 1.3rem;
  li {
    cursor: pointer;
    :hover {
      color: #E9B44C;
    }
    a {
      color: white;
      text-decoration: none;
    }
  }
}

footer {
  background-color: #1e3231;
  padding: 2em 0;
  color: #DBDBDB;
}

@keyframes moveDown {
  from { top: 0; opacity: 0.7; }
  to   { top: 10px; opacity: 0; }
}

.arrow-animation {
  position: relative;
  animation: moveDown 1.2s infinite;
  cursor: pointer;
}

.ml2 {
  font-weight: 900;
  font-size: 3.5em;
}

.ml2 .letter {
  display: inline-block;
  line-height: 1em;
}
</style>
