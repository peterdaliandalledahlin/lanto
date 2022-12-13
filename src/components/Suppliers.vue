<template>
    <v-container id="suppliers">
      <h1 class="title mb-2">Kök</h1>
      <v-row class="mt-3">
        <v-col v-for="kitchen in kitchens" :key="kitchen.id" cols="12" sm="6" lg="3">
          <v-card
            class="mx-auto"
            max-width="400"
            elevation="5"
          >
      <v-img       
        height="200px"
        :src="kitchen.img"
      >
        <!-- <v-card-title>Det här blir en bra dag</v-card-title> -->
      </v-img>
  
      <!-- <v-card-subtitle class="pb-0">
        Ev. information
      </v-card-subtitle> -->
  
      <!-- <v-card-text class="text--primary">
        <div class="text-h5">{{ supplier.type }}</div>
  
        <div>{{ supplier.title }}</div>
      </v-card-text> -->
  
      <v-card-actions>
        <v-btn
          color="#000"
          
          :href="kitchen.link"
          target="_blank"
        >
          Till hemsidan
        </v-btn>
  
      </v-card-actions>
    </v-card>
        </v-col>
      </v-row>
      <h1 class="title mt-3 mb-1">Bänkskivor</h1>
      <v-row class="mt-3">
        <v-col v-for="countertop in countertops" :key="countertop.id" cols="12" sm="6" lg="3">
          <v-card
            class="mx-auto"
            max-width="400"
            elevation="5"
          >
      <v-img       
        height="200px"
        :src="countertop.img"
      >
        <!-- <v-card-title>Det här blir en bra dag</v-card-title> -->
      </v-img>
  
      <!-- <v-card-subtitle class="pb-0">
        Ev. information
      </v-card-subtitle> -->
  
      <!-- <v-card-text class="text--primary">
        <div class="text-h5">{{ supplier.type }}</div>
  
        <div>{{ supplier.title }}</div>
      </v-card-text> -->
  
      <v-card-actions>
        <v-btn
          color="#000"
          
          :href="countertop.link"
          target="_blank"
        >
          Till hemsidan
        </v-btn>
  
      </v-card-actions>
    </v-card>
        </v-col>
      </v-row>
      <h1 class="title mt-3 mb-1">Beslag & tillbehör</h1>
      <v-row class="mt-3">
        <v-col v-for="design in designs" :key="design.id" cols="12" sm="6" lg="3">
          <v-card
            class="mx-auto"
            max-width="400"
            elevation="5"
          >
      <v-img       
        height="200px"
        :src="design.img"
      >
        <!-- <v-card-title>Det här blir en bra dag</v-card-title> -->
      </v-img>
  
      <!-- <v-card-subtitle class="pb-0">
        Ev. information
      </v-card-subtitle> -->
  
      <!-- <v-card-text class="text--primary">
        <div class="text-h5">{{ supplier.type }}</div>
  
        <div>{{ supplier.title }}</div>
      </v-card-text> -->
  
      <v-card-actions>
        <v-btn
          color="#000"
          
          :href="design.link"
          target="_blank"
        >
          Till hemsidan
        </v-btn>
  
      </v-card-actions>
    </v-card>
        </v-col>
      </v-row>
      <h1 class="title mt-3 mb-1">Diskbänkar</h1>
      <v-row class="mt-3">
        <v-col v-for="sink in sinks" :key="sink.id" cols="12" sm="6" lg="3">
          <v-card
            class="mx-auto"
            max-width="400"
            elevation="5"
          >
      <v-img       
        height="200px"
        :src="sink.img"
      >
        <!-- <v-card-title>Det här blir en bra dag</v-card-title> -->
      </v-img>
  
      <!-- <v-card-subtitle class="pb-0">
        Ev. information
      </v-card-subtitle> -->
  
      <!-- <v-card-text class="text--primary">
        <div class="text-h5">{{ supplier.type }}</div>
  
        <div>{{ supplier.title }}</div>
      </v-card-text> -->
  
      <v-card-actions>
        <v-btn
          color="#000"
          
          :href="sink.link"
          target="_blank"
        >
          Till hemsidan
        </v-btn>
  
      </v-card-actions>
    </v-card>
        </v-col>
      </v-row>
      <h1 class="title mt-3 mb-1">Vitvaror</h1>
      <v-row class="mt-3">
        <v-col v-for="appliance in appliances" :key="appliance.id" cols="12" sm="6" lg="3">
          <v-card
            class="mx-auto"
            max-width="400"
            elevation="5"
          >
      <v-img       
        height="200px"
        :src="appliance.img"
      >
        <!-- <v-card-title>Det här blir en bra dag</v-card-title> -->
      </v-img>
  
      <!-- <v-card-subtitle class="pb-0">
        Ev. information
      </v-card-subtitle> -->
  
      <!-- <v-card-text class="text--primary">
        <div class="text-h5">{{ supplier.type }}</div>
  
        <div>{{ supplier.title }}</div>
      </v-card-text> -->
  
      <v-card-actions>
        <v-btn
          color="#000"
          
          :href="appliance.link"
          target="_blank"
        >
          Till hemsidan
        </v-btn>
  
      </v-card-actions>
    </v-card>
        </v-col>
      </v-row>
      <h1 class="title mt-3 mb-1">Fläktkåpor</h1>
      <v-row class="mt-3">
        <v-col v-for="fancover in fancovers" :key="fancover.id" cols="12" sm="6" lg="3">
          <v-card
            class="mx-auto"
            max-width="400"
            elevation="5"
          >
      <v-img       
        height="200px"
        :src="fancover.img"
      >
        <!-- <v-card-title>Det här blir en bra dag</v-card-title> -->
      </v-img>
  
      <!-- <v-card-subtitle class="pb-0">
        Ev. information
      </v-card-subtitle> -->
  
      <!-- <v-card-text class="text--primary">
        <div class="text-h5">{{ supplier.type }}</div>
  
        <div>{{ supplier.title }}</div>
      </v-card-text> -->
  
      <v-card-actions>
        <v-btn
          color="#000"
          
          :href="fancover.link"
          target="_blank"
        >
          Till hemsidan
        </v-btn>
  
      </v-card-actions>
    </v-card>
        </v-col>
      </v-row>
      <h1 class="title mt-3">Garderober</h1>
      <v-row class="mt-3">
        <v-col v-for="wardrobe in wardrobes" :key="wardrobe.id" cols="12" sm="6" lg="3">
          <v-card
            class="mx-auto"
            max-width="400"
            elevation="5"
          >
      <v-img       
        height="200px"
        :src="wardrobe.img"
      >
        <!-- <v-card-title>Det här blir en bra dag</v-card-title> -->
      </v-img>
  
      <!-- <v-card-subtitle class="pb-0">
        Ev. information
      </v-card-subtitle> -->
  
      <!-- <v-card-text class="text--primary">
        <div class="text-h5">{{ supplier.type }}</div>
  
        <div>{{ supplier.title }}</div>
      </v-card-text> -->
  
      <v-card-actions>
        <v-btn
          color="#000"
          
          :href="wardrobe.link"
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
        kitchens: [
          { id: 1, img: 'claesson.png', icon: 'mdi-domain', title: 'Claesson kök', type: 'KÖK', link: 'https://www.claessonkok.se/'},
          { id: 2, img: 'smedstorp.png', icon: 'mdi-domain', title: 'Mora Armatur', type: 'KÖK', link: 'https://www.smedstorp.com/'},
        ],
        countertops: [
          { id: 1, img: 'granimar.webp', icon: 'mdi-domain', title: 'Granimar', type: 'BÄNKSKIVOR', link: 'https://www.granimar.se/'},
          { id: 2, img: 'lg.png', icon: 'mdi-domain', title: 'Nibe', type: 'BÄNKSKIVOR', link: 'https://www.lgcoll.se/'},  
        ],
        designs: [
          { id: 1, img: 'beslagdesign.svg', icon: 'mdi-domain', title: 'Beslag & Design', type: 'BESLAG & TILLBEHÖR', link: 'https://www.beslagdesign.se/'},
          { id: 2, img: 'linfalk.jpg', icon: 'mdi-domain', title: 'Linfalk', type: 'BESLAG & TILLBEHÖR', link: 'https://www.linfalk.se/'},  
        ],
        sinks: [
          { id: 1, img: 'nordictech.png', icon: 'mdi-domain', title: 'Nordic Tech', type: 'DISKBÄNKAR', link: 'https://www.nordic-tech.se/'},  
        ],
        appliances: [
          { id: 1, img: 'miele.png', icon: 'mdi-domain', title: 'Miele', type: 'VITVAROR', link: 'https://www.miele.se/'},
          { id: 2, img: 'witt.jpg', icon: 'mdi-domain', title: 'Witt Sverige', type: 'VITVAROR', link: 'https://www.wittsverige.se/'},
          { id: 3, img: 'lsbolagen.png', icon: 'mdi-domain', title: 'LS Bolagen', type: 'VITVAROR', link: 'https://lindstromsondenab.teamtailor.com/'},  
        ],
        fancovers: [
          { id: 1, img: 'fjaraskupan.png', icon: 'mdi-domain', title: 'Fjäråskupan', type: 'FLÄKTKÅPOR', link: 'https://fjaraskupan.se/'},
  
        ],
        wardrobes: [
          { id: 1, img: 'stirpe.jpg', icon: 'mdi-domain', title: 'Stirpe', type: 'GARDEROBER', link: 'https://stirpe.fi/sv/'},
        ],
      }
    }
  }
  </script>
  
  <style scoped>
@font-face {
  font-family: LibreBaskervilleItalic;
  src: url('../assets/fonts/LibreBaskerville-Italic.ttf');
}
.title {
    font-family: LibreBaskervilleItalic;
}
  </style>