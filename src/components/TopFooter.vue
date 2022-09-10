<template>
    <v-footer>
        <v-container>
            <v-row class="mt-3">
                <v-col v-for="contact in contact" :key="contact.id" cols="12" sm="4" lg="3">
                    <v-card
                        class="mx-auto text-center pa-5"
                        max-width="344"
                        min-width="344"
                        outlined
                        color="#333"
                        elevation="0"
                    >
                        <v-list-item three-line>
                            <v-list-item-content>
                                <v-list-item-title class="text-h5 mb-1">
                                    {{ contact.title}}
                                </v-list-item-title>
                                <v-list-item-subtitle class="text-h6">
                                    {{ contact.name}}
                                </v-list-item-subtitle>
                                <v-list-item-subtitle class="text-h6">
                                    {{ contact.address}}
                                </v-list-item-subtitle>
                                <v-list-item-subtitle class="text-h6"><a :href="`tel:${contact.phone1}`">{{contact.phone2}}</a></v-list-item-subtitle>
                                <v-list-item-subtitle class="text-h6"><a :href="`mailto:${contact.email}`">{{contact.email}}</a></v-list-item-subtitle>
                            </v-list-item-content>
    
                            <!-- <v-avatar>
                                <v-icon dark>
                                    {{ contact.icon }}
                                </v-icon>
                            </v-avatar> -->
                        </v-list-item>
    
                        <!-- <v-card-actions>
                        <v-btn
                            outlined
                            rounded
                            text
                        >
                            Kontakta
                        </v-btn>
                        </v-card-actions> -->
                    </v-card>
                </v-col>
            </v-row>
        </v-container>
    </v-footer>
</template>
  
  <script>
  import { defineComponent } from 'vue'
  
  export default defineComponent({
    name: 'top-footer',
    data() {
        return {
            contact: [
                { id: 1, icon: 'mdi-crown-circle', title: 'Lanto Kök & Bygg', address: 'Torggatan 28 C', zip: '745 31', postaddess: 'Enköping', email: ''},
                { id: 2, icon: 'mdi-file-document-edit', title: 'Kontakt', name: '', phone1: '+4617134000',phone2: '0171-340 00', email: 'info@kok-bygg.se'},
                { id: 3, icon: 'mdi-cash-100', title: 'Öppettider', name: 'Endast för enskilda visningar. Efter tidsbokning på;', phone1: '+4617134000', phone2: '0171-340 00', email: ''},
                // { id: 4, icon: 'mdi-account-arrow-left', title: 'Suppleant', name: 'Håkan Wallén', phone1: '+46705296107', phone2: '070-529 61 07', email: 'hakan@sevasta.se'},
                // { id: 5, icon: 'mdi-account-arrow-left', title: 'Suppleant', name: 'Kent Möller', phone1: '+46701625436', phone2: '070-162 54 36', email: 'arezzo953@hotmail.com'},
                // { id: 6, icon: 'mdi-calculator', title: 'Revisor', name: 'Lars Johansson', phone1: '+46705767763', phone2: '070-576 77 63', email: 'lars.johansson@live.com'},
                // { id: 7, icon: 'mdi-account-arrow-left', title: 'Suppleant', name: 'Barbro Vestin', phone1: '+46730765421', phone2: '073-076 54 21', email: 'bw505121@gmail.com'},
                // { id: 8, icon: 'mdi-swap-horizontal', title: 'Valberedning', name: 'Eva Blomkvist', phone1: '+46702564217', phone2: '070-256 42 17', email: ''},
                // { id: 9, icon: 'mdi-swap-horizontal', title: 'Valberedning', name: 'Mats Melander', phone: '+46707137714', phone: '070-713 77 14', email: ''},
                // { id: 10, icon: 'mdi-numeric', title: 'Organisationsnr.', name: '817000-8703', phone1: '', phone2: '', email: ''},
                // { id: 11, icon: 'mdi-numeric', title: 'Bankgiro', name: '320-0490', phone1: '', phone2: '', email: ''},
            ],
        }
    },
    components: {
      
    },
  })
</script>
  
<style scoped>
@font-face {
  font-family: LibreBaskervilleItalic;
  src: url('../assets/fonts/LibreBaskerville-Italic.ttf');
}
@font-face {
  font-family: MontserratRegular;
  src: url('../assets/fonts/Montserrat-Regular.ttf');
}
.v-row {
    justify-content: center !important;
}
.v-list-item-title {
    font-family: LibreBaskervilleItalic !important;
    color: floralwhite;
}
.v-list-item-subtitle {
    font-family: MontserratRegular !important;
    color: floralwhite;
}
.v-list-item-subtitle a {
    font-family: MontserratRegular !important;
    color: floralwhite;
}
.v-footer {
    padding: 0 !important;
    background-color: #333;
}
  </style>
  