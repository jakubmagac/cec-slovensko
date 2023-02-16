<template>
  <div class="py-16">
    <h1>Location</h1>
    <div>
      <p>IAESTE CEC 2023 will take place in Hrabovo which is a suburban part located in the west of Ružomberok. Its creation is related to the construction of a waterworks in the area for the purpose of supplying cotton plants. Tourism contributed to the development, which was related to the construction of the ski resort in Malinô-Brdo. In 1964, a cable car was built from Hrabov to Malinô-Brdo. Today, Hrabovo serves not only as the lower station of the aforementioned cable car, but also as an exit to Veľká Fatra. In addition to the cottage area, there are also many areas for recreation and sports. Currently, the construction of recreational buildings is being carried out in the vicinity of the water reservoir.</p>
      <v-carousel
        cycle
        height="400"
        hide-delimiter-background
        show-arrows-on-hover
        class="my-6"
      >
        <v-carousel-item
          v-for="(slide, i) in slides"
          :key="i"
        >
          <v-sheet
            color="transparent"
            height="100%"
          >
            <v-img
              :width="`100%`"
              :src="`/slider/${slide}`"
              cover
            />
          </v-sheet>
        </v-carousel-item>
      </v-carousel>
      <h2>
        How do I get there?
      </h2>
      <div
        style="background-color: #D91D5D; color: white; padding: 1em; box-shadow: 10px 10px 37px -17px rgba(0,0,0,0.75);
  border-radius: 6px;"
        class="mb-6">
        <p>Oh that’s quite simple. Once you cross the borders of Slovakia, just find the nearest road and stop a horse carriage. Local people are very kind and generous. They will have no problem with taking you to Ružomberok. </p>
        <p>Just kidding!</p>
      </div>
      <v-expansion-panels accordion class="mb-4">
        <v-expansion-panel>
          <v-expansion-panel-header>
            <h3>
              Train
            </h3>
          </v-expansion-panel-header>
          <v-expansion-panel-content>
            <p>You can get here easily from Bratislava or Košice by taking a fast train “Ex” to Ružomberok. More information about train/bus connections can be found here. Use this website to buy a train ticket. </p>
            <p>If you are traveling from Prague you can take Regiojet or LeoExpress.If you want, you can also take Flixbus from Budapest to Kosice. When you arrive in Ružomberok, take bus number 5 from the train station to “Hrabovo, konečná” which is the last stop and it is right next to the hotel. Bus leaves every hour. Use the Ubian app to see the departure time or buy public transport tickets.</p>
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>

      <v-expansion-panels accordion class="mb-4">
        <v-expansion-panel>
          <v-expansion-panel-header>
            <h3>
              Bus
            </h3>
          </v-expansion-panel-header>
          <v-expansion-panel-content>
            <p>Best way to get to Ružomberok by bus is by using Flixbus or you can search for buses here. Tickets are available on the bus.</p>
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>

      <v-expansion-panels accordion>
        <v-expansion-panel>
          <v-expansion-panel-header>
            <h3>
              Car
            </h3>
          </v-expansion-panel-header>
          <v-expansion-panel-content>
            <p>Easiest way to get here by car is to take the D1 highway. GPS location of the hotel: 49.070401, 19.272158</p>
            <ul class="mb-2">
              <li>
                <a href='https://goo.gl/maps/AqR4JoVVvBQRQHSu7'>
                  GPS route from Bratislava to CEC
                </a>
              </li>
              <li>
                <a href='https://goo.gl/maps/C36yG4FGDJ2HNDDS8'>
                  GPS route from Budapest to CEC
                </a>
              </li>
              <li>
                <a href='https://goo.gl/maps/LUfJTb12YHVGnubUA'>
                  GPS route from Prague to CEC
                </a>
              </li>
              <li>
                <a href='https://goo.gl/maps/MK1nEv7dingS5jfY9'>
                  GPS route from Warsaw to CEC
                </a>
              </li>
            </ul>
            <p>When you arrive to Ružomberok, take the bus number 5 from train station to “Hrabovo konečná”.</p>
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>

      <div class="mt-6">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2613.851717216377!2d19.267749330645866!3d49.07045322753446!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x4715a7e038824c0d%3A0x1098559da3b65b70!2sHotel%20Hrabovo!5e0!3m2!1ssk!2ssk!4v1676565035365!5m2!1ssk!2ssk"
          width="100%"
          height="450"
          style="border:0;"
          allowfullscreen=""
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LocationPage',
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
        'hotel_hrabovo1.jpg',
        'hotel_hrabovo2.jpg',
        'hotel_hrabovo3.jpg',
        'hotel_hrabovo4.jpg'
      ]
    }
  }
}
</script>

<style>

h1, h2 {
  text-transform: uppercase;
  margin-bottom: 1em;
}

.v-expansion-panel {
}
</style>
