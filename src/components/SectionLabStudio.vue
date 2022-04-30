<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-xs-12 col-lg-12 col-xl-6 gap-2">
        <h2>
          Press from <br />
          Watch Lab Studio
        </h2>
        <p>
          On the other hand, we denounce with righteous indignation and dislike
          men who are so gebuiled and demoralized by the charms of pleasure of
          the moment, so blinded by desirem that they cannot foresee the pain
          trouble
        </p>
      </div>
      <div class="d-none d-lg-block col-lg-12 col-xl-6 square">
        <div class="text">
          <h4>PRESS</h4>
          <h4 class="date">18 SETTEMBRE 2015</h4>
          <h3>Most Important Days on Watchlab</h3>

          <!-- buttons -->
          <div class="icons">
            <font-awesome-icon
              icon="fas fa-angle-left"
              class="carousel-control-prev"
              type="button"
              data-bs-target="#demo"
              data-bs-slide="prev"
            />
            <font-awesome-icon
              icon="fas fa-angle-right"
              class="carousel-control-next"
              type="button"
              data-bs-target="#demo"
              data-bs-slide="next"
            />
          </div>
        </div>

        <!-- slider -->
        <!-- Carousel -->
        <div id="demo" class="carousel slide" data-bs-ride="carousel">
          <!-- The slideshow/carousel -->
          <div class="carousel-inner">
            <div class="carousel-item active">
              <img
                src="../assets/img/factory.jpg"
                alt="Los Angeles"
                class="d-block w-100"
              />
            </div>
            <div class="carousel-item">
              <img
                src="../assets/img/factory2.webp"
                alt="Chicago"
                class="d-block w-100"
              />
            </div>
            <div class="carousel-item">
              <img
                src="../assets/img/factory4.jpg"
                alt="New York"
                class="d-block w-100"
              />
            </div>
          </div>
          <!-- /slider -->
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionLabStudio",
};
</script>

<style lang="scss" scoped>
@import "../style/partials/variables.scss";

@mixin centered {
  max-width: 85%;
  margin: auto;
}
@mixin description {
  color: $basic-color-3;
  font-family: "Merriweather";
  letter-spacing: 0.5px;
  font-size: 14px;
  line-height: 30px;
}
@mixin collection-title {
  font-family: "Montserrat-bold";
  font-size: 13px;
  letter-spacing: 2.5px;
}

.container-fluid {
  @include centered;
  padding-bottom: 100px;
  margin-top: 100px;
  h4 {
    @include collection-title;
  }
  .date {
    color: $button-color;
  }
  h2 {
    font-family: $font1;
    font-size: 9vmin;
    padding-bottom: 40px;
  }
  h3 {
    font-family: $font1;
  }
  p {
    @include description;
    padding-bottom: 220px;
    padding-right: 220px;
  }
  .square {
    background-color: $basic-color-4;
    position: relative;
    height: 660px;
  }
}
.carousel {
  top: 68%;
  right: 50%;
  transform: translateY(-50%);
  position: absolute;
  width: 500px;
  margin-left: 50px;
}
.carousel-item {
  img {
    height: 400px;
    object-fit: cover;
  }
}
.text {
  width: 250px;
  position: absolute;
  right: 0;
  top: 220px;
  h3 {
    padding-top: 30px;
  }
}
.icons {
  font-size: 15px;
  .carousel-control-next {
    color: black;
    padding-top: 200px;
  }
  .carousel-control-prev {
    color: black;
    padding-top: 200px;
  }
}
$breakpoint-smartphone: 576px; //sm
$breakpoint-ipad: 991px; //md
$breakpoint-pc: 1199px; //lg
$breakpoint-screen: 1400px; //xl

// fino a 1198 px
@media (max-width: $breakpoint-pc) {
  .container-fluid {
    .square {
      margin-top: -200px;
      height: 500px;
    }
    p {
      padding-right: 0px;
      padding-bottom: 220px;
    }
    .text {
      right: 30px;
      top: 50px;
    }
  }
  .carousel {
    top: 10%;
    left: 5%;
    transform: translateX(-10%);
  }
}

// da 0 fino a 991
@media (max-width: $breakpoint-ipad) {
  .container-fluid {
    p {
      padding-right: 0px;
      padding-bottom: 0;
    }
  }
}
// min 1199 a max 1400
@media only screen and (min-width: $breakpoint-pc) and (max-width: $breakpoint-screen) {
  .text {
    top: 50px;
    left: 50px;
  }
  .carousel {
    left: 0;
    width: 400px;
  }
  .carousel-item {
    img {
      height: 300px;
    }
  }
  .container-fluid {
    p {
      padding-right: 0px;
    }
  }
}
</style>
