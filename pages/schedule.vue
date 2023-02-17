<template>
  <v-container class="py-16" :style="$vuetify.breakpoint.mdAndDown ? 'margin-top: 40px' : 'margin-top: 80px'">
    <v-row justify="center">
      <v-col cols="12" sm="10" md="8" lg="6">
        <h1>Schedule</h1>
        <div class="d-flex" style="flex-direction: column;">
          <table class="mb-6">
            <tr>
              <td><h4>Friday May 26th</h4></td>
            </tr>
            <tr>
              <td>15:00 – 18:00</td>
              <td>Arrival</td>
            </tr>
            <tr>
              <td>18:00 – 19:00</td>
              <td>Dinner</td>
            </tr>
            <tr>
              <td>19:00 – 19:45</td>
              <td>Opening ceremony + CER presentation</td>
            </tr>
            <tr>
              <td>19:45 – 20:15</td>
              <td>Polka dancing</td>
            </tr>
            <tr>
              <td>20:15 – 00:00</td>
              <td>Party with minigames</td>
            </tr>
          </table>

          <table class="mb-6">
            <tr>
              <td><h4>Saturday May 27th</h4></td>
            </tr>
            <tr>
              <td>07:45 – 08:00</td>
              <td>Polka warm-up</td>
            </tr>
            <tr>
              <td>08:00 – 09:00</td>
              <td>Breakfast</td>
            </tr>
            <tr>
              <td>09:15 – 10:45</td>
              <td>WS1 / CER Representatives Meeting – part I</td>
            </tr>
            <tr>
              <td>10:45 – 11:00</td>
              <td>Break</td>
            </tr>
            <tr>
              <td>11:00 – 12:30</td>
              <td>WS1 / CER Representatives meeting – part II</td>
            </tr>
            <tr>
              <td>12:30 – 13:30</td>
              <td>Lunch</td>
            </tr>
            <tr>
              <td>13:30 – 14:15</td>
              <td>Power nap</td>
            </tr>
            <tr>
              <td>14:15 – 14:30</td>
              <td>Group photo</td>
            </tr>
            <tr>
              <td>14:30 – 16:00</td>
              <td>WS2 – part I</td>
            </tr>
            <tr>
              <td>16:00 – 16:15</td>
              <td>Break</td>
            </tr>
            <tr>
              <td>16:15 – 17:45</td>
              <td>WS2 – part II</td>
            </tr>
            <tr>
              <td>18:00 – 18:30</td>
              <td>Small dinner</td>
            </tr>
            <tr>
              <td>19:00 – 19:30</td>
              <td>IE preparation</td>
            </tr>
            <tr>
              <td>19:30 – …</td>
              <td>International evening</td>
            </tr>
          </table>

          <table class="mb-6">
            <tr>
              <td><h4>Sunday May 28th</h4></td>
            </tr>
            <tr>
              <td>08:45 – 09:00</td>
              <td>Polka warm-up</td>
            </tr>
            <tr>
              <td>09:00 – 10:30</td>
              <td>Breakfast</td>
            </tr>
            <tr>
              <td>10:30 – 11:30</td>
              <td>Closing ceremony</td>
            </tr>
            <tr>
              <td>12:00</td>
              <td> Departure</td>
            </tr>
            <tr>
              <td>13:00 – …</td>
              <td>Post-conference tour</td>
            </tr>
          </table>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'SchedulePage'
}
</script>

<style>
table {
  /* border: 1px solid #0c0c0c; */
  box-shadow: 10px 10px 37px -17px rgba(0,0,0,0.75);
  border-radius: 6px;
  background-color: #D91D5D;;
  color: #fff;
  padding: 2em;
}
</style>
