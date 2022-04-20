<template>
    <button class="carousel-control left" @click="$emit('prev')">Prev</button>
    <button class="carousel-control right" @click="$emit('next')">Next</button>
</template>

<script>
    export default {
        emits: ['prev', 'next'] 
    }
</script>

<style>
    .carousel-control {
        background-color: hsl(0, 0%, 0%, 0.5);    
        border: none;
        display: inline-block;
        position: absolute;
        height: 50px;
        width: 70px;    
        top: calc(50% - 25px);
        color: white;
        cursor: pointer;
        z-index: 99;
    }
    .right {
        right: 0;
    }
    .left {
        left: 0;
    }
</style>