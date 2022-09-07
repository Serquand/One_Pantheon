<template>
    <div id="training" class="formation-main-container">
        <h2>Formations proposées</h2>
        <div class="formation-content">
            <div
                :key="formation"
                v-for="formation in formations"
                class="formation"
            >
                <img :src="formation.image" :alt="formation.title" />
                <h4>{{ formation.title }}</h4>
            </div>
        </div>
    </div>
</template>

<script>
import { formations as allOurFormations } from '../information.json'
export default {
    setup() {
        const formations = allOurFormations
        return { formations }
    }
}   
</script>

<style>
    #training {
        padding-top: 20px;
        margin-top: -20px;            
    }

    .formation-main-container {
        margin-bottom: 75px;
    }

    .formation-main-container h2 {
        margin: 100px auto 45px;
    }

    .formation-main-container h4 {
        text-align: center;
    }

    .formation-content {
        display: flex;
        justify-content: space-around;
        width: 90%;
        margin: auto;
    }

    .formation {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .formation img {
        width: 64px;
        height: auto;
        margin: 10px 0;
    }

    @media all and (max-width: 1300px) {
        .formation-content {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 35px;
        }
    }

    @media all and (max-width: 650px) {
        .formation-content {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 35px;
        }
    }
</style>