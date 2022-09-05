<template>
    <div id="services">
        <h2>Nos services</h2>
        <div class="services-content">
            <div
                :key="service"
                v-for="service in allOurServices">
                <Service 
                    :description="service.description"
                    :title="service.title"    
                />
            </div>
        </div>
    </div>
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
    }
}
</script>

<style>
</style>