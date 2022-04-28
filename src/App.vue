<template>
  <div id="app">
    <Navbar />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";

export default {
  name: "App",
  components: {
    Navbar,
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
</style>
