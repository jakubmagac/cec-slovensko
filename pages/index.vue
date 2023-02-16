<template>
  <v-container class="py-16">
    <v-row>
      <v-col cols="12" md="6">
        <v-img
          lazy-src="/janosik_logo.jpg"
          src="/janosik_logo.jpg"
          max-width="300px"
          max-height="300px"
          class="mb-6 image-animation"
          style="position: relative; z-index: 1;"
        />
      </v-col>
      <v-col cols="12" md="6" class="d-flex" style="flex-direction: column; justify-content: center;">
        <p>Dear IAESTE Board, Representatives, Workshop leaders and participants,</p>
        <p>We are very pleased to invite you to the 46th IAESTE Central European Convention, taking place in Slovakia from 26th to 28th May 2023!</p>
        <p>See you soon in Slovakia!</p>
        <p>Your Organizing Team</p>
        <v-btn
          to='/register'
          style="background-color: #D91D5D; color: #f9f9f9;"
          text
        >
          <strong>Register Now</strong>
        </v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>

<style>
.image-animation {
  position: relative;
  cursor: pointer;
  /* animation-name: imageAnimation; */
  /* animation-duration: 8s; */
  /* animation-iteration-count: infinite; */
}

.register-button {
  border: 1px solid #0c0c0c;
  padding: 1em;
  background-color: white;
  cursor: pointer;
}

@keyframes imageAnimation {
  0% { left: 0px; top: 0px; }
  25% { left: 10px; top: 10px }
  50% { left: 0px; top: 40px }
  75% { left: 10px; top: 10px }
  100% { left: 0px; top: 0px; }
}
</style>
