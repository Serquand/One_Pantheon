<template>
    <div id="app-main-container">
        <HeaderBar />
        <Landing />
        <Services />
        <Formation />
        <FooterBar />
        <div id="full-size"></div>
    </div>
</template>

<script>
import HeaderBar from './components/HeaderBar.vue'
import FooterBar from './components/FooterBar.vue';
import Services from './components/Services.vue'
import Formation from './components/Formation.vue'
import Landing from './components/Landing.vue'

export default {
    name: 'App',
    components: {
        HeaderBar, 
        FooterBar, 
        Services, 
        Formation, 
        Landing
    }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto+Serif:opsz,wght@8..144,100&display=swap');

*, *::after, *::before {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Roboto Serif', serif;
}

html {
    scroll-behavior: smooth;
}

#full-size {
    height: 100%;
    width: 100%;
    position: fixed;
    background: linear-gradient(180deg, rgba(70,123,157,1) 50%, rgba(104,159,188,1) 100%);
    top: 0;
    left: 0;
    z-index: -50;
}

*:not(.text) {
    color: white;
}
</style>
