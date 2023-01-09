<template>
  <v-parallax
    src="lanto-header.jpg"
    id="home"
  >
    <div class="d-flex flex-column fill-height justify-center align-center text-white">
      <v-img class="my-3" width="150" height="150" src="logo.png" />
    </div>
  </v-parallax>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'home',

})
</script>
