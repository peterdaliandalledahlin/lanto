<template>
  <v-container id="gallery">
    <v-carousel hide-delimiters>
        <v-carousel-item
            v-for="(item,i) in items"
            :key="i"
            :src="item.src"
            cover
        ></v-carousel-item>
  </v-carousel>
  </v-container>
</template>

<script>
    export default {
      data () {
        return {
          items: [
            {
              src: 'gallery1.jpg',
            },
            {
              src: 'gallery2.jpg',
            },
            {
              src: 'gallery3.jpg',
            },
            {
              src: 'gallery4.jpg',
            },
            {
              src: 'gallery5.jpg',
            },
            {
              src: 'gallery6.jpg',
            },
            {
              src: 'gallery7.jpg',
            },
            {
              src: 'gallery8.jpg',
            },
            {
              src: 'gallery9.jpg',
            },
            {
              src: 'gallery10.jpg',
            },
            {
              src: 'gallery11.jpg',
            },
            {
              src: 'gallery12.jpg',
            },
            {
              src: 'gallery13.jpg',
            },
            {
              src: 'gallery14.jpg',
            },
          ],
        }
      },
    }
  </script>

<style scoped>
@media screen and (min-width: 992px) {
    .v-window.v-theme--light.v-carousel {
        height: 800px !important;
    }
}
/*
@media (min-width: 576px) {}
@media (min-width: 768px) {}
@media (min-width: 992px) {}
@media (min-width: 1200px) {}
@media (min-width: 1400px) {}

@media screen and (max-width: 992px) {}
@media screen and (max-width: 600px) {}
*/
/* .v-window.v-theme--light.v-carousel {
    height: 800px !important;
} */
</style>