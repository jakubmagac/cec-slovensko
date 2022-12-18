<template>
  <v-container :style="$vuetify.breakpoint.smAndDown ? 'padding: 2em 0' : 'padding: 2em 0'">
    <v-row justify="center" align="center">
      <v-col cols="11" md="10">
        <p>On this page you can find details about all workshops at CECarinthia</p>
        <v-expansion-panels accordion>
          <v-expansion-panel
            v-for="w in workshops"
            :key="w.id"
          >
            <v-expansion-panel-header>
              <h2 style="color: #6EC1E4;">
                {{ w.name }}
              </h2>
            </v-expansion-panel-header>
            <v-expansion-panel-content>
              {{ w.description }}
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'IndexPage',
  data () {
    return {
      workshops: [
        {
          id: 0,
          name: 'Full day workshop',
          description: 'Interactive case study that outlines how an efficient exchange cycle could be done compared to our classic exchange cycle (by  Reza Goldansaz, Kushagra Sharma, Valentina Carrasco Rosales, Olga Legacka, Dzhamshed Saidov (half day), Thomas Faltner (half day) ) Interactive case study that outlines how an efficient exchange cycle could be done compared to our classic exchange cycle : Nowadays the needs of employers and students has changed, and expectations have risen. Therfore the core business of our association, Exchange, requires a careful treatment, in order to satisfy our stakeholders. Do you think our current model (classic exchange) fulfills the nowadays world’s expectations? How can we move towards a more agile and intelligent process and develop as a world top exchange program? If you want to experience a different level of knowledge sharing, and get a glance of how the future of IAESTE working model can look like, and contribute to shaping of it, don’t miss this unique workshop! During this workshop, we will share how top exchange programs work (benchmarking), possibilities to be applied within our association (brainstorming), and successful case studies.'
        }
      ]
    }
  }
}
</script>
