<template>
    <div class="service-container">
        <div class="service">
        <div class="content"></div> 
        <div class="overlay"></div>
        <p class="text">{{ title }}</p> 
        </div>
        <h4 class="description">{{  description }}</h4>
    </div>
</template>

<script>
export default {
    props: {
        title: {
            type: String, 
            required: true
        }, 

        description: {
            type: String, 
            required: true
        }
    }
}
</script>

<style>
.service-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 50px;
}

.service {
    height: 210px;
    width: 210px;
    clip-path: polygon(0 30%, 50% 0, 100% 30%, 100% 70%, 50% 100%, 0 70%);
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    overflow: hidden;
}

.content {
    height: 200px;
    width: 200px;
    clip-path: polygon(0 30%, 50% 0, 100% 30%, 100% 70%, 50% 100%, 0 70%);
    background-color: white;
}

.text {
    color: black;
}

.overlay {
    top: 0;
    width: 100%;
    height: 0%;
    background-color: black;
    position: absolute;
    z-index: -5;
    animation: appBox 4s ease 1 forwards;
}

.text {
    position: absolute;
    height: fit-content;
    top: 50%;
    transform: translateY(-50%);
    width: 100%;
    text-align: center;
    font-size: 35px;
    font-weight: 600;
    font-variant-caps: small-caps;
}

.description {
    font-weight: 500;
    font-size: 19px;
    width: 80%;
    margin: 15px auto auto auto;
    text-align: center;
}

@keyframes appBox {
    from { height: 0%; } 
    to { height: 100%; }
}
</style>