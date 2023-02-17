<template>
  <v-app dark>
    <v-container class="py-16" :style="$vuetify.breakpoint.mdAndDown ? 'margin-top: 40px' : 'margin-top: 80px'">
      <v-row>
        <v-col style="display: flex; align-items: center; justify-content: center;">
          <div>
            <h1 style="color: black; text-align: center; margin-bottom: 0;">
              Sorry that page doesn't exist :(
            </h1>
            <dir style="text-align: center;">
              <NuxtLink to="/">
                Return to Home Page
              </NuxtLink>
            </dir>
            <div style="display: flex; justify-content: center;">
              <v-img
                src="/404.webp"
                max-width="500px"
                width="100%"
              />
            </div>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>
export default {
  name: 'EmptyLayout',
  layout: 'empty',
  props: {
    error: {
      type: Object,
      default: null
    }
  },
  data () {
    return {
      pageNotFound: '404 Not Found',
      otherError: 'An error occurred'
    }
  },
  head () {
    const title =
      this.error.statusCode === 404 ? this.pageNotFound : this.otherError
    return {
      title
    }
  }
}
</script>

<style scoped>
h1 {
  font-size: 20px;
}
</style>
