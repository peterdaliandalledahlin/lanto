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
                class="mx-4"
                icon="mdi-home"
                variant="plain"
                ></v-btn>
                <v-btn
                class="mx-4"
                icon="mdi-email"
                variant="plain"
                ></v-btn>
                <v-btn
                class="mx-4"
                icon="mdi-instagram"
                variant="plain"
                ></v-btn>
            </v-card-text>

      <v-divider></v-divider>

      <v-card-text>
        © Copyright - {{ new Date().getFullYear() }} — <strong>Lanto Kök & Bygg</strong>
      </v-card-text>
        </v-card>
      </v-footer>
</template>
  
  <script>
  import { defineComponent } from 'vue'
  
  export default defineComponent({
    name: 'bottom-footer',
    components: {
      
    },
  })
  </script>
  <style scoped>
    .v-footer {
        padding: 0 !important;
    }
  </style>
  