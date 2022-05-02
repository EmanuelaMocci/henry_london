<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col">
        <div class="text">
          <h2>WATCH/LAB</h2>
        </div>
      </div>
    </div>

    <div class="row width">
      <div class="col-xs-12 col-sm-6 col-xl-3">
        <div class="row">
          <div class="col">
            <ul class="el">
              <li>Watch/Lab - Innovation brings success</li>
              <li>Via Bologna 5, Milan</li>
              <li>Italy</li>
            </ul>
          </div>
        </div>
      </div>
      <div class="col-xs-12 col-sm-6 col-xl-3">
        <div class="row">
          <div class="col">
            <ul class="right">
              <li>About us</li>
              <li>Brand</li>
              <li>Projects</li>
              <li>Magazine</li>
            </ul>
          </div>
        </div>
      </div>

      <div class="col-xs-12 col-sm-6 col-xl-3">
        <div class="row">
          <div class="col">
            <ul class="right">
              <li>Press</li>
              <li>Contacts</li>
              <li>Privacy Policy</li>
              <li>Search</li>
            </ul>
          </div>
        </div>
      </div>

      <div class="col-xs-12 col-sm-6 col-xl-3">
        <div class="row">
          <div class="col">
            <ul class="right">
              <li>T. +39 392 9133937</li>
              <li>M. <span> info@watch-lab.it</span></li>
              <li class="styled">FACEBOOK</li>
              <li class="styled">INSTAGRAM</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    <Copyright />
  </div>
</template>

<script>
import Copyright from "./Copyright.vue";

export default {
  name: "Footer",
  components: {
    Copyright,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/partials/variables.scss";

@mixin centered {
  max-width: 85%;
  margin: auto;
}

.container-fluid {
  @include centered;
  background-color: $basic-color-5;
  color: $basic-color-1;
  padding: 0;
  .text {
    h2 {
      font-family: $font3;
      color: $basic-color-1;
      letter-spacing: 2px;
      font-size: 4vmin;
    }
  }
  margin-bottom: 100px;
  ul {
    padding-left: 80px;
    li {
      list-style: none;
      font-family: $font1;
      color: $button-color;
      line-height: 40px;
      span {
        text-decoration: underline;
        text-underline-offset: 5px;
        text-decoration-thickness: 0.5px;
      }
    }
    .styled {
      font-family: $font3;
      font-size: 13px;
      letter-spacing: 2.5px;
    }
  }
  .text {
    padding: 80px 0 50px 80px;
  }
}
.width {
  width: 90%;
  padding-bottom: 100px;
}
</style>
