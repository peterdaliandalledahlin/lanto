<template>
  <v-container>
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

<style>

</style>