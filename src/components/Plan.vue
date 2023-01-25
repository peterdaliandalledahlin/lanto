<template>
    <v-parallax
      src="panovision-bg.jpg"
    >
      <div class="d-flex flex-column fill-height justify-center align-center text-white">
        <v-btn @click="scrollToLink('contact')" color="#D7B46A" aria-label="scrolla till kontakt">Planera ditt köksköp - boka tid</v-btn>
      </div>
    </v-parallax>
  </template>
  
  <script>
  import { defineComponent } from 'vue'
  
  export default defineComponent({
    name: 'plan',
  
    components: {
      
    },
    methods: {
      scrollToLink(link) {
        document.getElementById(link).scrollIntoView({ behavior: "smooth", block: 'nearest' })
      }
    }
  })
  </script>
  <style scoped>
.d-flex.flex-column.fill-height.justify-center.align-center.text-white {
  min-height: 200px !important;
}
  
  </style>
  