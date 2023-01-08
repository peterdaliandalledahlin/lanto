<template>
    <v-container fluid id="drawing-help">
        <v-card
            plain
            class="pa-5"
        >
            <h1 class="title mb-2">Vi ritar ert kök.</h1>
            <p class="bread">
              Vi hjälper er att rita och planera det nya köket. Förbered er med en enkel måttskiss,
              fundera över ert behov och önskemål avseende vitvaror, arbetsytor, köksdesign m.m.
              så skapar vi gemensamt ert nya drömkök.<br />
              Tid bokas med Torbjörn Lanto, Kök &amp; Bygg på tel: 0171-340 00.<br />
              Vid ett första möte i vår utställning på Torggatan 28 C, visar vi vårt sortiment och går
              igenom era önskemål och förutsättningar avseende ert nya kök.
              För den som önskar, ritas sedan det nya köket upp i vårt ritprogram. Vi går
              tillsammans igenom förslaget och gör justeringar utifrån era önskemål.<br />
            <span class="font-weight-bold">För detta debiteras 5000:- som sedan återbetalas vid eventuellt köksköp.</span>
            </p>
        </v-card>
    </v-container>
</template>

<script>
export default {

}
</script>

<style scoped>
/* @import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@700&family=Work+Sans:wght@700;800&display=swap'); */
/* @font-face {
  font-family: LibreBaskervilleRegular;
  src: url('../assets/fonts/LibreBaskerville-Regular.ttf');
} */
@font-face {
  font-family: LibreBaskervilleItalic;
  src: url('../assets/fonts/LibreBaskerville-Italic.ttf');
}
@font-face {
  font-family: MontserratRegular;
  src: url('../assets/fonts/Montserrat-Regular.ttf');
}
.title {
    font-family: LibreBaskervilleItalic;
}
.bread {
    font-family: MontserratRegular;
    line-height: 2;
}

</style>