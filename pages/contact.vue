<template>
  <v-container class="py-16" :style="$vuetify.breakpoint.mdAndDown ? 'margin-top: 40px' : 'margin-top: 80px'">
    <v-row justify="center">
      <v-col cols="12" sm="10" md="8" lg="6">
        <div class="d-flex justify-center">
          <div style=" border-radius: 100%;" class="mb-6">
            <v-img
              lazy-src="/sano.png"
              src="/sano.png"
              max-width="200px"
              max-height="200px"
              style="border-radius: 100%; margin: 0 auto; border: 5px solid #D91D5D;"
            />
          </div>
        </div>
        <div>
          <h3>Hello I am Sano</h3>
          <p>Dear IAESTE Board, Representatives, Workshop leaders and participants,</p>
          <p>We are very pleased to invite you to the 46th IAESTE Central European Convention, taking place in the Slovak Republic from 13th to 15th May 2022!</p>
          <p>See you soon in the Slovak Republic!</p>
          <p>Your Organizing Team of IAESTE CECkia</p>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'ContactPage'
}
</script>
