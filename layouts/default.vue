<template>
  <v-app>
    <header
      style="background: url('./poster.jpg'); background-attachment: fixed; min-height: 100vh; background-size: cover; display: flex; align-items: flex-start;"
    >
      <div style="background-color: #000000A0; width: 100%; height: 100%; ">
        <v-container fluid style="position: relative; z-index: 2; height: 100%;">
          <v-row class="navigation">
            <v-col cols="1">
              <v-img
                lazy-src="/logo.png"
                src="/logo.png"
                max-height="75"
                min-height="75"
                max-width="75"
                min-width="75"
              />
            </v-col>
            <v-spacer />
            <v-col cols="9" style="alignItems: center;" class="d-flex">
              <!-- <ul class="menu">
                <li @click="scrollHome">Home</li>
                <li @click="scrollRegistration">Registration</li>
                <li @click="scrollLocation">Location</li>
                <li @click="scrollSchedule">Schedule</li>
                <li @click="scrollWorkshops">Workshops</li>
              </ul> -->
            </v-col>
          </v-row>
          <v-row style="height: 100%; display: flex; alignItems: center;">
            <v-col class="text-center" style="position: relative; top: -100px;">
              <h1
                :style="animation ? '' : 'visibility: hidden;'"
                class="main-heading ml2 font-weight-light"
              >
                46th Central European Convention
              </h1>
              <template v-if="$nuxt.$route.name === 'index'">
                <h2 style="color: #fff; font-size: 1.3rem;" class="mt-4 mb-8 font-weight-light">
                  19th - 21th of May 2022
                </h2>
              </template>
              <v-icon x-large color="white" class="arrow-animation" @click="scrollContent">mdi-chevron-down</v-icon>
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
    scrollContent () {
      this.$refs.content.scrollIntoView({ behavior: 'smooth', block: 'start', inline: 'nearest' })
    },
    scrollHome () {
      this.$refs.home.scrollIntoView({ behavior: 'smooth', block: 'start', inline: 'nearest' })
    },
    scrollRegistration () {
      this.$refs.register.scrollIntoView({ behavior: 'smooth', block: 'start', inline: 'nearest' })
    },
    scrollLocation () {
      this.$refs.location.scrollIntoView({ behavior: 'smooth', block: 'start', inline: 'nearest' })
    },
    scrollSchedule () {
      this.$refs.schedule.scrollIntoView({ behavior: 'smooth', block: 'start', inline: 'nearest' })
    },
    scrollWorkshops () {
      this.$refs.workshops.scrollIntoView({ behavior: 'smooth', block: 'start', inline: 'nearest' })
    }
  }
}
</script>

<style lang="scss">
.layout-container {
  /* font-size: 1.5rem; */
  padding: 4em 0;

  @media screen and (max-width: 960px)  {
    padding: 2em 0;
  }
}

.navigation {
  width: 100%; z-index: 5;
}

.menu {
  display: flex;
  list-style: none;
  width: 100%;
  color: white;
  justify-content: space-around;
  font-size: 1.2rem;
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

.main-heading {
  font-size: 3rem;
  color: #fff;
  overflow-wrap: break-word;
  word-wrap: break-word;
  word-break: break-word;

  @media screen and (max-width: 960px)  {
    font-size: 2rem;
  }

  @media screen and (max-width: 600px)  {
    font-size: 1.7rem;
  }
}
</style>
