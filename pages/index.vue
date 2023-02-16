<template>
  <div class="d-flex py-16">
    <div style="position: relative; left: -50px;">
      <v-img
        lazy-src="/janosik_logo.jpg"
        src="/janosik_logo.jpg"
        max-width="300px"
        max-height="300px"
        class="mb-6 image-animation"
        style="position: relative; z-index: 1;"
      />
      <div style="width: 300px; height: 300px; background-color: #f2c4e3; position: absolute; bottom: 0px; left: 20px; z-index: 0; box-shadow: 10px 10px 37px -17px rgba(0,0,0,0.75); border-radius: 6px;" />
    </div>
    <div style="display: flex; flex-direction: column; justify-content: center;">
      <p>Dear IAESTE Board, Representatives, Workshop leaders and participants,</p>
      <p>We are very pleased to invite you to the 46th IAESTE Central European Convention, taking place in Slovakia from 26th to 28th May 2023!</p>
      <p>See you soon in Slovakia!</p>
      <p>Your Organizing Team</p>
      <v-btn
        to='/register'
        style="background-color: #f2c4e3;"
        text
      >
        <strong>Register Now</strong>
      </v-btn>
    </div>
  </div>
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
