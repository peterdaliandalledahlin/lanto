<template>
    <v-container id="suppliers">
      <h1 class="title mb-2">Kök</h1>
      <v-row class="mt-3">
        <v-col v-for="kitchen in kitchens" :key="kitchen.id" cols="12" sm="6" lg="3">
          <v-card
            class="mx-auto fill-height"
            max-width="400"
            elevation="5"
          >
      <v-img
        v-if="!kitchen.img == ''"      
        height="200px"
        :src="kitchen.img"
      >
        <!-- <v-card-title>Det här blir en bra dag</v-card-title> -->
      </v-img>
  
      <!-- <v-card-subtitle class="pb-0">
        Ev. information
      </v-card-subtitle> -->
  
      <v-card-text class="text--primary" v-if="!kitchen.title == ''">
        <div class="text-h4 text-center mb-2">{{ kitchen.type }}</div>
  
        <div>{{ kitchen.title }}</div>
      </v-card-text>
  
      <v-card-actions v-if="!kitchen.link == ''">
        <v-btn
          aria-label="länk till köksleverantörer"
          color="#000"
          :href="kitchen.link"
          target="_blank"
          v-show="!kitchen.link == ''"
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
        aria-label="länk till köksbänksleverantörer"
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
          aria-label="länk till lverantörer av beslag och design"
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
          aria-label="länk till lverantörer av diskbänkar"
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
          aria-label="länk till leverantörer av vitvaror"
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
          aria-label="länk till leverantörer av fläktkåpor"
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
          aria-label="länk till leverantörer av garderober"
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
          { id: 1, img: 'claesson.png', icon: 'mdi-domain', title: '', type: '', link: 'https://www.claessonkok.se/'},
          { id: 2, img: 'smedstorp.png', icon: 'mdi-domain', title: '', type: '', link: 'https://www.smedstorp.com/'},
          { id: 3, img: '', icon: 'mdi-domain', title: 'Här kommer vi att presentera designade kök och inredningar som tagits fram tillsammans med lokala leverantörer och samarbetspartners, utifrån kundens unika krav och önskemål. Under januari månad kommer bilder på kök och skjutdörrar med namn ”Kesudden” att presenteras.', type: 'ENAköket', link: ''},
        ],
        countertops: [
          { id: 1, img: 'granimar.webp', icon: 'mdi-domain', title: '', type: 'BÄNKSKIVOR', link: 'https://www.granimar.se/'},
          { id: 2, img: 'lg.png', icon: 'mdi-domain', title: '', type: 'BÄNKSKIVOR', link: 'https://www.lgcoll.se/'},  
        ],
        designs: [
          { id: 1, img: 'beslagdesign.svg', icon: 'mdi-domain', title: '', type: 'BESLAG & TILLBEHÖR', link: 'https://www.beslagdesign.se/'},
          { id: 2, img: 'linfalk.jpg', icon: 'mdi-domain', title: '', type: 'BESLAG & TILLBEHÖR', link: 'https://www.linfalk.se/'},  
        ],
        sinks: [
          { id: 1, img: 'nordictech.png', icon: 'mdi-domain', title: '', type: 'DISKBÄNKAR', link: 'https://www.nordic-tech.se/'},  
        ],
        appliances: [
          { id: 1, img: 'miele.png', icon: 'mdi-domain', title: '', type: 'VITVAROR', link: 'https://www.miele.se/'},
          { id: 2, img: 'witt.jpg', icon: 'mdi-domain', title: '', type: 'VITVAROR', link: 'https://www.wittsverige.se/'},
          { id: 3, img: 'lsbolagen.png', icon: 'mdi-domain', title: '', type: 'VITVAROR', link: 'https://lindstromsondenab.teamtailor.com/'},  
        ],
        fancovers: [
          { id: 1, img: 'fjaraskupan.png', icon: 'mdi-domain', title: '', type: 'FLÄKTKÅPOR', link: 'https://fjaraskupan.se/'},
  
        ],
        wardrobes: [
          { id: 1, img: 'stirpe.jpg', icon: 'mdi-domain', title: '', type: 'GARDEROBER', link: 'https://stirpe.fi/sv/'},
        ],
      }
    }
  }
  </script>
  
  <style scoped>
@font-face {
  font-family: LibreBaskervilleItalic;
  font-display: swap;
  src: url('../assets/fonts/LibreBaskerville-Italic.ttf');
}
.title {
  font-family: LibreBaskervilleItalic;
}
  /* .v-container#suppliers {
    display: flex;
    flex-direction: column;
    align-items: stretch;
  } */
/* .v-container#suppliers {
  width: 100%;
  display: grid;
  gap: 1rem;
  grid-template-columns: repeat(auto-fill, min-max(100px,1fr));
  grid-auto-rows: 50px;
} */
  </style>