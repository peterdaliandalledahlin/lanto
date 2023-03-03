<template>
    <v-container fluid id="campaign">
        <h1>SKAPA DITT DRÖMKÖK TILLSAMMANS MED OSS!</h1>
        <div class="wrapper">
            <span>Kök</span><span>Bygg</span> 
        </div>
        <h2>Vi är med dig hela vägen från design till montering</h2>
        <h3><span>Kökskampanj</span> under mars månad, då vi har öppet;</h3>
        <p>Lördag 10:00-13:00 och Måndag 12:00-18:00, övrig tid efter tidsbokning</p>
        <p>Torggatan 28C, info@kok-bygg.se, 0171-340 00</p>
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
.v-container {
    text-align: center;
    background-color: #231F20;
}
h1 {
    font-size: clamp(1rem, -0.875rem + 8.333vw, 2rem);
}
h2 {
    font-size: clamp(.8rem, -0.875rem + 8.333vw, 1.5rem);
}
h1, h3 > span {
    color: #FEF200;
}
h2, h3, p {
    color: #fff;
    /* #FEF200 */
}
.wrapper {
    display: flex;
    justify-content: center;
}
.wrapper > span {
    color: #fff;
}
/* .wrapper > span:nth-child(1) {
    justify-content: right;
    transform: rotate(-90deg);
    justify-content: flex-end;
} */
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