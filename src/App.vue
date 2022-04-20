<template>
  <carousel-body :slides="slides"></carousel-body>
  <!-- <FormRedLyon /> -->
  <!-- <HamburgerMenu /> -->
</template>

<script>
import CarouselBody from './components/carrousel/CarouselBody.vue'


// import HamburgerMenu from './components/HamburgerMenu.vue'
// import FormRedLyon from './components/FormRedLyon.vue'


export default {
  name: 'App',
  components: {
    CarouselBody

  },
  data() {
    return {
      slides: [
        "https://picsum.photos/id/1035/900/400",
        "https://picsum.photos/id/1036/900/400",
        "https://picsum.photos/id/1037/900/400",
        "https://picsum.photos/id/1038/900/400",
        "https://picsum.photos/id/1039/900/400",
        // "./assets/img-carrousel/Imagen1.jpg",
        // "./assets/img-carrousel/Imagen2.jpg",
        // "./assets/img-carrousel/Imagen3.jpg",
        // "./assets/img-carrousel/Imagen4.jpg",
        // "./assets/img-carrousel/Imagen5.jpg"
      ],
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}
</style>
