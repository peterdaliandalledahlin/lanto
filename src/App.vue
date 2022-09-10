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
        v-for="(item, i) in items"
        :key="i"
        :value="item"
        active-color="primary"
      >
        <template v-slot:prepend>
          <v-icon :icon="item.icon"></v-icon>
        </template>

        <v-list-item-title v-text="item.text"></v-list-item-title>
      </v-list-item>
    </v-list>

      <!-- <v-list
        dense
        nav
      >
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title @click="$vuetify.goTo(item.link, drawer = false,  {duration: 500, easing: 'easeInOutCubic'})">{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list> -->
    </v-navigation-drawer>

    <v-app-bar app color="#D7B46A">
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Lanto Kök & Bygg</v-toolbar-title>

      <v-spacer></v-spacer>

        <v-btn icon>
          <v-icon>mdi-magnify</v-icon>
        </v-btn>

        <!-- <v-btn icon>
          <v-icon>mdi-heart</v-icon>
        </v-btn>

        <v-btn icon>
          <v-icon>mdi-dots-vertical</v-icon>
        </v-btn> -->
    </v-app-bar>

    <v-main>
      <Jumbotron />
      <Infobox />
      <Plan />
      <DrawingHelp />
      <Suppliers />
      <Gallery />
      <Contact />
      <Map />
      <TopFooter />
      <BottomFooter />
    </v-main>
  </v-app>
</template>

<script>
import Jumbotron from './components/Jumbotron.vue'
import Infobox from './components/Infobox.vue'
import Plan from './components/Plan.vue'
import DrawingHelp from './components/DrawingHelp.vue'
import Suppliers from './components/Suppliers.vue'
import Gallery from './components/Gallery.vue'
import Contact from './components/Contact.vue'
import Map from './components/Map.vue'
import TopFooter from './components/TopFooter.vue'
import BottomFooter from './components/BottomFooter.vue'
export default {
  name: 'App',
  components: { Jumbotron, Infobox, Plan, DrawingHelp, Suppliers, Gallery, Contact, Map, TopFooter, BottomFooter },
  data: () => ({
    drawer: null,
    items: [
        { text: 'Hem', icon: 'mdi-home', link: '#home' },
        { text: 'Rithjälp', icon: 'mdi-draw', link: '#draw' },
        { text: 'Audience', icon: 'mdi-account' },
        { text: 'Conversions', icon: 'mdi-flag' },
      ],
    // items: [
    //       { title: 'Hem', icon: 'mdi-home', link: '#home' },
    //       { title: 'Boka', icon: 'mdi-calendar-range', link: '#book' },
    //       { title: 'Prislista', icon: 'mdi-cash-100', link: '#pricelist' },
    //       { title: 'Aktuellt', icon: 'mdi-bell-ring', link: '#events'  },
    //       { title: 'Aktiviteter', icon: 'mdi-human-female-dance', link: '#activities' },
    //       { title: 'Sponsring', icon: 'mdi-cash-100', link: '#sponsorship' },
    //       { title: 'Sponsorer', icon: 'mdi-cash-100', link: '#sponsors' },
    //       { title: 'Hitta till oss', icon: 'mdi-map-marker', link: '#find-us' },
    //       { title: 'Kontakta oss', icon: 'mdi-account-box', link: '#contact' },
    //       { title: 'Galleri', icon: 'mdi-view-gallery', link: '#gallery' },
    //       { title: 'Tidslinje', icon: 'mdi-timeline', link: '#timeline' },
    //       { title: 'Ladda ner', icon: 'mdi-file-download', link: '#download' },
    //     ],
  }),
}
</script>

<style scoped>

</style>