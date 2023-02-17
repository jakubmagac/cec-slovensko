<template>
  <v-container class="py-16" :style="$vuetify.breakpoint.smAndDown ? 'margin-top: 40px' : 'margin-top: 80px'">
    <v-row justify="center">
      <v-col cols="12" sm="10" md="8" lg="6">
        <h1>Registration</h1>
        <p>The registration will start on March 13th. Check our social sites for more info.</p>
        <h3>Fees</h3>
        <p>The fees for next IAESTE CEC in Slovakia are as follows:</p>
        <div
          class="my-8"
          style="display: grid;"
          :style="$vuetify.breakpoint.smAndDown
            ? 'grid-template-columns: 1fr; grid-gap: 30px;'
            : 'grid-template-columns: 1fr 1fr 1fr; grid-gap: 20px;'"
        >
          <div class="card">
            <p><strong>130 EUR</strong></p>
            <p>IAESTE CER<br> Full Members </p>
          </div>

          <div class="card">
            <p><strong>132 EUR</strong></p>
            <p>IAESTE CER<br> Associate Members </p>
          </div>

          <div class="card">
            <p><strong>134 EUR</strong></p>
            <p>Others</p>
          </div>
        </div>

        <p>The IAESTE CER Member Countries are listed below:</p>
        <p>IAESTE CER Full Members: Austria, Bosnia and Herzegovina, Croatia, Czech Republic, Germany, Hungary, Poland, Slovakia, Slovenia</p>
        <p>IAESTE CER Associate Members: Macedonia, Turkey</p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'RegisterPage'
}
</script>

<style>
.card {
  background-color: #D91D5D;
  padding: 1em;
  text-align: center;
  border: 0;
  border-radius: 8px;
  opacity: 0.9;
  color: white;
  box-shadow: 6px 7px 19px 4px rgb(91, 91, 91)
}
</style>
