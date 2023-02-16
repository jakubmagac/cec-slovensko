<template>
  <v-container :style="$vuetify.breakpoint.smAndDown ? 'padding: 2em 0' : 'padding: 2em 0'">
    <v-row justify="center">
      <v-col cols="11" md="10">
        <h1 class="mb-6">Location</h1>
        <p>IAESTE CEC 2023 will take place in Hrabovo which is a suburban part located in the west of Ružomberok. Its creation is related to the construction of a waterworks in the area for the purpose of supplying cotton plants. Tourism contributed to the development, which was related to the construction of the ski resort in Malinô-Brdo. In 1964, a cable car was built from Hrabov to Malinô-Brdo. Today, Hrabovo serves not only as the lower station of the aforementioned cable car, but also as an exit to Veľká Fatra. In addition to the cottage area, there are also many areas for recreation and sports. Currently, the construction of recreational buildings is being carried out in the vicinity of the water reservoir.</p>
        <h2>*Hotel Hrabovo na Google Maps*</h2>

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

        <h2>The Tale of Ružomberok</h2>
        <p>The river, along which the king and his entourage had been traveling for several days, had no end. It just gradually got used up and the banks became steeper. The horsemen, tired and exhausted since they trotted along the barely perceptible road, found mostly deserted areas – the Tatars had withdrawn, but they were left with plundered and almost deserted valleys. The further north, the more striking the landscape became, stunning with the untamed allure of spruce and pine forests and rushing clear streams. The hills, emerging one by one, reflected in dark green on the light blue surface, as if they did not end anywhere. They thickened on the horizon, and more and more, in an effort to deter the newcomers. They threatened to get lost. "If it continues like this, we will return," thought the young king. "The wild forests are only worth hunting." He still tries to go around the narrow bend of the water ribbon with the passengers along the path that rises behind the backs of the walls to the top. The landscape suddenly opened up in front of them in a semi-hill and a semi-circle. On the wide tray of the horizon, the valley is bordered by emerald mountains and in the middle, like an eye in the silver horseshoe of the river that flowed around it, a huge ruby - a hill covered with red flowers.</p>
      </v-col>
    </v-row>
    <v-row justify="center">
      <v-col cols="11" md="10">
        <div>
          <img
            :width="`100%`"
            src="/historical_ruzomberok.jpg"
            cover
          >
          <p>
            In the flood of sun it shone as if it had been ravaged by the most destructive fire. The king and his party were enthralled. Because of the beauty in the middle of the basin, it was worth the arduous journey. The young monarch remembered his nurse - he was a little boy when she told him about a distant miraculous mountain glowing with purple flowers. Allegedly, once every hundred years, she releases one of her beauties cursed in the scales to a hero from the royal family. This miracle deserves to be seen up close. They went down, where the path widened so that they could spur the horses into a gallop. They stopped under a hill covered with fiery red wild roses. He resembled a resting monk with his hood pulled deep over his forehead. Here they saw what could not be discerned from a distance - as if copying the ring of ancient ramparts, purple was broken below the peak by a pearl necklace of rose-blooming arrow bushes.
          </p>
          <p>
            A doe was making her way between the sparkling pink pearls. She was barely noticed in the flood of flowers - she was all white. The family giggled quietly. The king, an avid hunter, subconsciously reached into his quiver and drew the string. The arrow whistled. Something like a scream, like a wail, like an echo was heard. When they reached the place, they found the girl under the bushes among the fallen leaves. She lay pale, lifeless, and beautiful. No injuries. The unhappy king looked after the horsemen. What now? There was one among them whom they knew understood the language of animals and birds. A poor little man, striking with piercing eyes and an aquiline nose. He started looking around. In the bushes above, he found what he was probably subconsciously looking for - a red rose pierced by an arrow right in the heart. He handed it to his master and indicated with a gesture that he should place the flower on the lying one. It happened. A tiny drop flowed from the pierced rose onto the white chest. Is it blood? Red gradually seeped in, spread - the girl's shoulders, shoulders and cheeks turned pink. Her eyelashes fluttered and then she inhaled. She opened her eyes and saw the king bowed down, surprised and delighted. He gave a hand to the miraculously awakened woman, helped her up and placed her in the saddle. After returning home, the young king married a beautiful woman. He founded a settlement in a place under a hill covered with red flowers, which later grew into a city. A rose, pierced by an arrow, lands in his coat of arms.
          </p>
          <h2>
            How do I get there?
          </h2>
          <p>Oh that’s quite simple. Once you cross the borders of Slovakia, just find the nearest road and stop a horse carriage. Local people are very kind and generous. They will have no problem with taking you to Ružomberok. </p>
          <p>Just kidding!</p>
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
                <p>
                  GPS route from Bratislava to CEC: https://goo.gl/maps/AqR4JoVVvBQRQHSu7
                  GPS route from Budapest to CEC: https://goo.gl/maps/C36yG4FGDJ2HNDDS8
                  GPS route from Prague to CEC: https://goo.gl/maps/LUfJTb12YHVGnubUA
                  GPS route from Warsaw to CEC: https://goo.gl/maps/MK1nEv7dingS5jfY9
                </p>
                <p>From Ružomberok to the Hotel</p>
                <p>When you arrive to Ružomberok, take the bus number 5 from train station to “Hrabovo konečná”.</p>
              </v-expansion-panel-content>
            </v-expansion-panel>
          </v-expansion-panels>
        </div>
      </v-col>
    </v-row>
  </v-container>
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
}
</style>
