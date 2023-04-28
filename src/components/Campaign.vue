<template>
    <v-container fluid id="campaign">
        <h1>KÖKSKAMPANJ</h1>
        <h2>FÅ <span>2.000:-</span><span> AV VARJE 10.000:- SOM KÖKET KOSTAR</span></h2>
        <h3>för att köpa vitvaror eller bänkskivor från vårt sortiment under kampanjperioden!</h3>
        <div class="wrapper">
            <span>Kök</span><span>Bygg</span> 
        </div>
        <p>Öppet efter tidsbokning ring 0171-340 00</p>
        <p class="mb-3">Torggatan 28C &bull; info@kok-bygg.se &bull; 0171-340 00</p>
        <p class="welcome">Välkommen till köksutställningen</p>
        <!-- <p>Köp kök under kampanj-perioden och <span>få 2.000:- per 10.000:-</span> som köket kostar att nyttja vid köp av vitvaror från vårt sortiment från <span>Miele</span> och <span>Witt</span></p> -->
        <!-- <p>Köp kök under kampanj-perioden och <span>få 2.000:- per 10.000:-</span> att nyttja vid köp av vitvaror från vårt sortiment från <span>Miele</span> och <span>Witt</span></p> -->
        <!-- <p>Gratis köksplanering under kampanj-perioden (ordinarie pris = 5.000:-)</p> -->
    </v-container>
</template>

<script setup>

</script>

<style scoped>
@font-face {
  font-family: Agan;
  font-display: swap;
  src: url('../assets/fonts/Agan.woff');
}
@font-face {
  font-family: LibreBaskerville-Italic;
  font-display: swap;
  src: url('../assets/fonts/LibreBaskerville-Italic.ttf');
}
.v-container {
    text-align: center;
    background-color: #231F20;
}
h1 {
    background-color: #EBC501;
    color: #fff;
    font-size: clamp(1.5rem, -0.875rem + 8.333vw, 2.2rem);
    display: inline-block;
    padding: 0 10px;
}
h2 {
    font-size: clamp(.8rem, -0.875rem + 8.333vw, 2rem);
    color: #fff;
}
h2 > span:nth-child(1) {
    color: #EBC501;
}
h2 > span:nth-child(2) {
    font-size: clamp(.6rem, -0.875rem + 8.333vw, 1.6rem);
}
h3 {
    font-size: clamp(.2rem, -0.875rem + 8.333vw, 1rem);
    color: #fff;
}
p {
    color: #fff;
}
.welcome {
    font-family: 'LibreBaskerville-Italic', sans-serif;
    font-size: clamp(.6rem, -0.875rem + 8.333vw, 1.6rem);
    background-color: #EBC501;
    color: black;
    display: inline-block;
    padding: 0 30px;
}
.wrapper {
    display: flex;
    justify-content: center;
}
.wrapper > span {
    color: #fff;
}
.wrapper > span:nth-child(1) {
    font-family: Agan, sans-serif;
    font-size: 3rem;
}
.wrapper > span:nth-child(1)::before {
    content: 'Lanto';
    display: inline-block;
    font-size: .8rem;
    transform: rotate(-90deg);
    position: relative;
    top: -12px;
    right: -15px;
    color: #FEF200;
}
.wrapper > span:nth-child(2) {
    font-family: Agan, sans-serif;
    font-size: 2.5rem; 
}
.wrapper > span:nth-child(2)::before {
    content: '&';
    color: #fff;
    font-size: 3rem;
    background-color: #FEF200;
    width: 2rem;
    height: 2rem;
    border-radius: 50%;
    font-weight: bolder;
    padding-left: 10px;
    padding-right: 10px;
}
</style>