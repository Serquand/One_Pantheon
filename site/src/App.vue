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
*, *::after, *::before {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
    /* background-color: #689fbc; */
    /* background: linear-gradient(180deg, rgba(70,123,157,1) 50%, rgba(104,159,188,1) 100%); */
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
