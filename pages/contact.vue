<template>
  <div class="py-16">
    <div>
      <v-img
        lazy-src="/sano.png"
        src="/sano.png"
        max-width="200px"
        max-height="200px"
        class="mb-6"
        style="border-radius: 100%; margin: 0 auto; border: 5px solid #f2c4e3;"
      />
    </div>
    <div style="display: flex; flex-direction: column; justify-content: center;">
      <p>Dear IAESTE Board, Representatives, Workshop leaders and participants,</p>
      <p>We are very pleased to invite you to the 46th IAESTE Central European Convention, taking place in the Slovak Republic from 13th to 15th May 2022!</p>
      <p>See you soon in the Slovak Republic!</p>
      <p>Your Organizing Team of IAESTE CECkia</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ContactPage'
}
</script>

<style>
.image-animation:hover {
  position: relative;
  cursor: pointer;
  animation-name: imageAnimation;
  animation-duration: 3s;
  animation-iteration-count: infinite;
}

@keyframes imageAnimation {
  0% { left: 0px; top: 0px; }
  50% { left: 10px; top: 10px }
  100% { left: 0px; top: 40px }
}
</style>
