<template>
  <div id="app">
    <circles-to-rhombuses-spinner
      :animation-duration="1200"
      :circles-num="3"
      :circle-size="15"
      color="#c6b5a1"
      v-if="loading"
    />
    <template v-else>
      <Navbar />
      <Hero />
      <Main />
      <Footer />
    </template>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Hero from "./components/Hero.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";
import { CirclesToRhombusesSpinner } from "epic-spinners";

export default {
  name: "App",
  components: {
    Navbar,
    Hero,
    Main,
    Footer,
    CirclesToRhombusesSpinner,
  },
  data() {
    return {
      loading: true,
    };
  },
  async mounted() {
    await new Promise((r) => setTimeout(r, 2000));
    this.loading = false;
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

.circles-to-rhombuses-spinner {
  margin: 0;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 99;
}
</style>
