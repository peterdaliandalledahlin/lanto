<template>
    <v-dialog
        v-model="dialog"
        transition="dialog-top-transition"
        min-width="750"
        >
        <v-card
        class="mx-auto"
        max-width="auto"
    >
            <v-img
            :src="kampanj"
            height="200px"
            cover
            ></v-img>

            <v-card-title>
            Top western road trips
            </v-card-title>

            <v-card-subtitle>
            1,000 miles of wonder
            </v-card-subtitle>

            <v-card-actions>
                <v-btn color="primary" block @click="dialog = false">Close Dialog</v-btn>
            </v-card-actions>
        </v-card>
    </v-dialog>
</template>

<script setup>
import { ref } from 'vue'
import kampanj from '../assets/kokskampanj-mars-2023.jpg'

const dialog = ref(true)

</script>

<style scoped>

</style>