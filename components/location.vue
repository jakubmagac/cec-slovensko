<template>
  <v-container :style="$vuetify.breakpoint.smAndDown ? 'padding: 2em 0' : 'padding: 2em 0'">
    <v-row justify="center" align="center">
      <v-col cols="11" md="10">
        <h4>Location</h4>
        <p>Do you like the picture on our website ? Well then you should definitely join the 45th CEC in Austria, because this is where the conference will take place – in the most beautiful region of Austria, called Carinthia.</p>
        <p>The venue is located on the biggest lake in Carinthia and from the accommodation we can directly access the lake, called “Wörthersee”.</p>
        <p>You can find more information about the hostel on the website or check some of the pictures here.</p>
        <v-carousel
          cycle
          height="400"
          hide-delimiter-background
          show-arrows-on-hover
        >
          <v-carousel-item
            v-for="(slide, i) in slides"
            :key="i"
          >
            <v-sheet
              :color="colors[i]"
              height="100%"
            >
              <v-row
                class="fill-height"
                align="center"
                justify="center"
              >
                <div class="text-h2">
                  {{ slide }} Slide
                </div>
              </v-row>
            </v-sheet>
          </v-carousel-item>
        </v-carousel>
        <div style="border: 1px solid #000; text-align: center;" class="mt-4 py-4">
          <h4>How to get there</h4>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'LocationComponent',
  data () {
    return {
      colors: [
        'indigo',
        'warning',
        'pink darken-2',
        'red lighten-1',
        'deep-purple accent-4'
      ],
      slides: [
        'First',
        'Second',
        'Third',
        'Fourth',
        'Fifth'
      ]
    }
  }
}
</script>
