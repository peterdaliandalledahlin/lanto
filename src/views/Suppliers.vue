<template>
    <v-container id="suppliers">
      <h4>Leverantörer</h4>
      <v-row class="mt-3">
        <v-col v-for="supplier in suppliers" :key="supplier.id" cols="12" sm="4" lg="3">
          <v-card
            class="mx-auto"
            max-width="400"
            elevation="5"
          >
      <v-img
        
        height="200px"
        :src="supplier.img"
      >
        <!-- <v-card-title>Det här blir en bra dag</v-card-title> -->
      </v-img>
  
      <!-- <v-card-subtitle class="pb-0">
        Ev. information
      </v-card-subtitle> -->
  
      <v-card-text class="text--primary">
        <div class="text-h5">{{ supplier.title}}</div>
  
        <div>Ev. annan information</div>
      </v-card-text>
  
      <v-card-actions>
        <v-btn
          color="#000"
          
          :href="supplier.link"
          target="_blank"
        >
          Till hemsidan
        </v-btn>
  
      </v-card-actions>
    </v-card>
        </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script>
  export default {
    name: 'suppliers',
    data() {
      return {
        suppliers: [
                  { id: 1, img: 'claesson.png', icon: 'mdi-domain', title: 'Claesson kök', link: 'https://www.claessonkok.se/'},
                  { id: 2, img: 'haga.jpg', icon: 'mdi-domain', title: 'Haga Kök', link: 'https://www.hagakoket.se/'},
                  { id: 3, img: 'smedstorp.png', icon: 'mdi-domain', title: 'Mora Armatur', link: 'https://www.smedstorp.com/'},
                  { id: 4, img: 'sjostrands.png', icon: 'mdi-domain', title: 'Grohe', link: 'https://www.sjostrandsgranit.sv/'},
                  { id: 5, img: 'lechner.png', icon: 'mdi-domain', title: 'Ifö', link: 'https://www.mylechner.de/se/'},
                  { id: 6, img: 'lg.png', icon: 'mdi-domain', title: 'Nibe', link: 'https://www.lgcoll.se/'},
                  { id: 7, img: 'decosteel.png', icon: 'mdi-domain', title: 'Gustavsberg', link: 'https://decosteel.se/'},
                  { id: 8, img: 'intra.png', icon: 'mdi-domain', title: 'Ido', link: 'https://www.intra-teka.com/svenska'},
                  { id: 9, img: 'nordictech.png', icon: 'mdi-domain', title: 'CTC', link: 'https://www.nordic-tech.se/'},
                  { id: 10, img: 'fjaraskupan.png', icon: 'mdi-domain', title: 'Inr', link: 'https://fjaraskupan.se/'},
                  { id: 11, img: 'beslagdesign.svg', icon: 'mdi-domain', title: 'Inr', link: 'https://www.beslagdesign.se/'},
                  { id: 12, img: 'linfalk.jpg', icon: 'mdi-domain', title: 'Inr', link: 'https://www.linfalk.se/'},
                  { id: 13, img: 'miele.png', icon: 'mdi-domain', title: 'Inr', link: 'https://www.miele.se/'},
                  { id: 14, img: 'agafalcon.jpg', icon: 'mdi-domain', title: 'Inr', link: 'https://agafalcon.com/en'},
                  { id: 15, img: 'elgiganten.jpg', icon: 'mdi-domain', title: 'Inr', link: 'https://elgiganten.se/'},
                  { id: 16, img: 'neff.png', icon: 'mdi-domain', title: 'Inr', link: 'https://www.neff-home.com/se/'},
                  { id: 17, img: 'smeg.png', icon: 'mdi-domain', title: 'Inr', link: 'https://www.smeg.com/se'},
                  { id: 18, img: 'lsbolagen.png', icon: 'mdi-domain', title: 'Inr', link: 'https://lindstromsondenab.teamtailor.com/'},
                  { id: 19, img: 'stirpe.jpg', icon: 'mdi-domain', title: 'Inr', link: 'https://stirpe.fi/sv/'},
  
              ],
      }
    }
  }
  </script>
  
  <style scoped>
  
  </style>