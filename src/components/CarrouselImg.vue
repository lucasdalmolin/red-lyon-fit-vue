<template>
    <div>
        <a href=""><img src="../assets/img-carrousel/parrot.jpg" alt=""></a>
        <a href=""><img src="../assets/img-carrousel/gallo.jpg" alt=""></a>
        <a href=""><img src="../assets/img-carrousel/owl.jpg" alt=""></a>
        <a href=""><img src="../assets/img-carrousel/barn-owl.jpg" alt=""></a>
        <a href=""><img src="../assets/img-carrousel/bird.jpg" alt=""></a>
    </div>
</template>

<script>
    export default {
        name: 'CarrouselImg',
        data() {

        }
    }

</script>

<style>

    img {
        display: flex;
        flex-direction: row;
        width: 400px;
        height: auto;
        transition: ease-in-out 500ms;
    }

    img:hover {
        width: 500px;
    }
</style>