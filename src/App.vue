<template>
  <div id="app">
    <Navbar />
    <Hero />
    <Main />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Hero from "./components/Hero.vue";
import Main from "./components/Main.vue";

export default {
  name: "App",
  components: {
    Navbar,
    Hero,
    Main,
  },
};
</script>

<style>
@font-face {
  font-family: "Montserrat";
  src: local("Montserrat"),
    url(./font/Montserrat-Regular.ttf) format("truetype");
}
@font-face {
  font-family: "Montserrat-bold";
  src: local("Montserrat"), url(./font/Montserrat-Bold.ttf) format("truetype");
}
@font-face {
  font-family: "Miller";
  src: local("Miller"), url(./font/Miller-Display_30501.ttf) format("truetype");
}
@font-face {
  font-family: "Merriweather";
  src: local("Merriweathert"),
    url(./font/Merriweather-Regular.ttf) format("truetype");
}
</style>
