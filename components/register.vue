<template>
  <v-container :style="$vuetify.breakpoint.smAndDown ? 'padding: 2em 0' : 'padding: 2em 0'">
    <v-row justify="center" align="center">
      <v-col cols="11" md="10" class="text-center">
        <h2>Countdown until 46th CEC - hosted by IAESTE Slovakia</h2>

        <p class="my-6">The second registration round will be open until the 04th of September. </p>
        <v-btn
          style="background-color: #F2C4E3;"
          elevation="2"
          :class="$vuetify.breakpoint.smAndDown ? 'my-6' : 'my-12'"
        >
          Join the CEC in Austria
        </v-btn>
        <p class="text-left">Your registration will be valid once your regional representative or national secretary has confirmed your attendance. When your spot is confirmed an email with the payment information will be sent. The deadline for the payment will be the 16th of September. After the payment is made, you will have secured your spot at #CECarinthia 2022 and can start packing!</p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'RegisterComponent'
}
</script>
