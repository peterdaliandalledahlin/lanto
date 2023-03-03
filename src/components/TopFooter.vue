<template>
    <v-footer>
        <v-container>
            <v-row class="mt-3">
                <v-col v-for="contact in contact" :key="contact.id" cols="12" sm="6" lg="3">
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
                                <v-list-item-subtitle v-if="contact.zip || contact.postaddress" class="text-h6">
                                    {{ contact.address}}<br />
                                    {{ contact.zip}} {{ contact.postaddress}}
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
                { id: 1, icon: 'mdi-crown-circle', title: 'Lanto Kök & Bygg', address: 'Torggatan 28 C', zip: '745 31', postaddress: 'Enköping', email: ''},
                { id: 2, icon: 'mdi-file-document-edit', title: 'Kontakt', name: '', phone1: '+4617134000',phone2: '0171-340 00', email: 'info@kok-bygg.se'},
                { id: 3, icon: 'mdi-cash-100', title: 'Öppettider', name: 'Endast för enskilda visningar. Efter tidsbokning på;', phone1: '+4617134000', phone2: '0171-340 00', email: ''}
            ],
        }
    },
  })
</script>
  
<style scoped>
@font-face {
  font-family: LibreBaskervilleItalic;
  font-display: swap;
  src: url('../assets/fonts/LibreBaskerville-Italic.ttf');
}
@font-face {
  font-family: MontserratRegular;
  font-display: swap;
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
  