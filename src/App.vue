<template>
  <v-app id="inspire">
    <v-navigation-drawer
      v-model="drawer"
      app
      color="#D7B46A"
      bottom
      temporary
    >
    <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="text-h6">
            Lanto Kök & Bygg
          </v-list-item-title>
          <v-list-item-subtitle>
            Vårt koncept "smart" - köp monterat & klart
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list density="compact">
        <v-list-subheader>LÄNKAR</v-list-subheader>

        <v-list-item
          v-for="item in items"
          :key="item.id"
          :value="item"
          active-color="#3E2723"
        >
          <template v-slot:prepend>
            <v-icon :icon="item.icon"></v-icon>
          </template>

          <v-list-item-title @click="scrollToLink(item.link), drawer = !drawer">{{item.text}}</v-list-item-title>
        </v-list-item>
      </v-list>

    </v-navigation-drawer>

    <v-app-bar class="elevation-0" density="compact">
      <!-- <v-toolbar-title>Snabbkontakt</v-toolbar-title> -->
      <v-spacer></v-spacer>
      <v-chip
      class="d-none d-sm-flex"
      color="#D7B46A"
      text-color="#000"
      variant="outlined"
      prepend-icon="mdi-hammer-screwdriver"
      href="https://skatteverket.se/privat/fastigheterochbostad/rotarbeteochrutarbete.4.2e56d4ba1202f95012080002966.html?q=rotavdrag"
      target="_blank"
      >
      30% ROT-avdrag
      </v-chip>
      <v-btn
      aria-label="ring 0171-34000"
      prepend-icon="mdi-phone"
      @click.prevent="handlePhoneNumber"
    >
      0171-340 00
    </v-btn>
    <v-btn
      prepend-icon="mdi-email"
      @click.prevent="handleMail"
      aria-label="öppna e-post"
    >
      info@kok-bygg.se
    </v-btn>
  </v-app-bar>

    <v-app-bar app color="#D7B46A">
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Lanto Kök & Bygg</v-toolbar-title>

      <v-spacer></v-spacer>

        <v-btn @click="scrollToLink('concept-smart')" icon aria-label="scrolla till koncept smart">
          <v-icon>mdi-head-lightbulb</v-icon>
        </v-btn>

    </v-app-bar>

    <v-main>
      <!-- <router-view /> -->
      <Jumbotron />
      <Infobox />
      <Plan />
      <DrawingHelp />
      <Storage />
      <ConceptSmart />
      <Suppliers />
      <Gallery />
      <Contact />
      <Map />
      <TopFooter />
      <BottomFooter />     
    </v-main>
  </v-app>
</template>

<script setup>
import { ref } from 'vue'
import Jumbotron from './components/Jumbotron.vue'
import Infobox from './components/Infobox.vue'
import Plan from './components/Plan.vue'
import DrawingHelp from './components/DrawingHelp.vue'
import Storage from './components/Storage.vue'
import Suppliers from './components/Suppliers.vue'
import Gallery from './components/Gallery.vue'
import Contact from './components/Contact.vue'
import Map from './components/Map.vue'
import TopFooter from './components/TopFooter.vue'
import BottomFooter from './components/BottomFooter.vue'
import ConceptSmart from './components/ConceptSmart.vue'

const drawer = ref(null)

const items = ref([
  { id: 1, text: 'Hem', icon: 'mdi-home', link: 'home' },
  { id: 2, text: 'Koncept "Smart"', icon: 'mdi-head-lightbulb', link: 'concept-smart' },
  { id: 3, text: 'Rithjälp', icon: 'mdi-draw', link: 'drawing-help' },
  { id: 4, text: 'Förvaring', icon: 'mdi-dresser', link: 'storage' },
  { id: 5, text: 'Galleri', icon: 'mdi-animation', link: 'gallery' },
  { id: 6, text: 'Kontakt', icon: 'mdi-email', link: 'contact' },
  { id: 7, text: 'Hitta till oss', icon: 'mdi-map-marker', link: 'map' },
  { id: 8, text: 'Leverantörer', icon: 'mdi-hammer-screwdriver', link: 'suppliers' },
])
  
const scrollToLink = (link) => {
  document.getElementById(link).scrollIntoView({ behavior: "smooth", block: 'end', inline: 'nearest' })
}

const handlePhoneNumber = () => {
  window.open('tel:+4617134000', '_self')
}

const handleMail = () => {
  window.open('mailto:info@kok-bygg.se', '_self')
}

</script>
