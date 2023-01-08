<template>
    <v-footer>
      <v-card
        elevation="0"
        rounded="0"
        width="100%"
        class="text-center"
        color="#D7B46A"
      >
          <v-card-text>
            <v-btn
            @click="scrollToLink('home')"
            class="mx-4"
            icon="mdi-home"
            variant="plain"
            ></v-btn>
            <v-btn
            href="mailto:info@kok-bygg.se"
            class="mx-4"
            icon="mdi-email"
            variant="plain"
            ></v-btn>
            <v-btn
            href="https://www.instagram.com/lantokok_bygg/"
            target="_blank"
            class="mx-4"
            icon="mdi-instagram"
            variant="plain"
            ></v-btn>
            <v-btn
            href="https://www.facebook.com/lantokokbygg"
            target="_blank"
            class="mx-4"
            icon="mdi-facebook"
            variant="plain"
            ></v-btn>
          </v-card-text>

      <v-divider></v-divider>

      <v-card-text>
        © Copyright - {{ new Date().getFullYear() }} — <strong>Lanto Kök & Bygg</strong> made by peterdahlindesign@gmail.com
        <!--
        <v-img
          :width="width"
          src="logotype_peterdahlindesign.png"
          cover
        ></v-img>
        -->
      </v-card-text>
    </v-card>
  </v-footer>
</template>
  
  <script>
  import { defineComponent } from 'vue'
  
  export default defineComponent({
    name: 'bottom-footer',
    data: () => ({
      //width: 50,
      //aspectRatio: 16 / 9,
    }),
    methods: {
      scrollToLink(link) {
        document.getElementById(link).scrollIntoView({ behavior: "smooth", block: 'nearest' })
      }
    }
  })
  </script>
  <style scoped>
    .v-footer {
        padding: 0 !important;
    }
  </style>
  