<template>
    <section id="services">
        <h2>Nos services</h2>
        <div class="services-content">
            <div
                :key="service"
                v-for="service in allOurServices"
                :class="['bloc-service', 'service-' + (service.title.startsWith('/') ? 'incubateur' : service.title)]" 
            >
                <Service 
                    :description="service.description"
                    :title="service.title"    
                />
            </div>
        </div>
    </section>
</template>

<script>
import Service from './Service.vue';
import { services } from '../information.json'

export default {
    components: {
        Service
    }, 

    setup() {
        const allOurServices = services
        return { allOurServices }
    },
}
</script>

<style>
    #services {
        padding-top: 50px;
        margin-top: -50px;
    }

    .services-content {
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        width: 90%;
        margin: auto;
    }
</style>