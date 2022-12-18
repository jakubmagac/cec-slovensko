<template>
  <v-container :style="$vuetify.breakpoint.smAndDown ? 'padding: 2em 0' : 'padding: 2em 0'">
    <v-row justify="center" align="center">
      <v-col cols="11" md="10">
        <h1>CEC Schedule</h1>
        <v-img
          lazy-src="/schedule.png"
          src="/schedule.png"
          class="mb-6"
        />
        <h4>What is IAESTE CEC?</h4>
        <p>The IAESTE Central European Convention (CEC) is the major international event of the IAESTE Central European Region (CER) and it is happening twice every year in a rotation schedule, so each country will organize the event. IAESTE members of all CER countries meet to learn from each other and discuss future plans.</p>
        <h4>IAESTE CER</h4>
        <p>IAESTE Central European Region’s vision is to provide more high quality opportunities for students’ development. We support their personal and professional growth by offering them paid work placement abroad. Further on by volunteering for our member countries students can develop their leadership and communication skills.</p>
        <p>More details about IAESTE can be found here: https://iaeste.org/</p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'ScheduleComponent'
}
</script>
