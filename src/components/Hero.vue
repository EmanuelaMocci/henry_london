<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col hero-container">
        <div class="hero">
          <div class="text">
            <h4>LONDON COLLECTION SEASON</h4>
            <h1 class="title">
              New Selection Of <br />
              Henry London
            </h1>
            <h5>An estimable experience in the modern collection house</h5>
            <button>Discover</button>
          </div>
        </div>
        <!-- slider -->
        <div
          id="carouselExampleControls"
          class="carousel slide"
          data-bs-ride="carousel"
        >
          <div class="carousel-inner">
            <div class="carousel-item active">
              <img
                src="../assets/img/watch3.webp"
                class="d-block w-100"
                alt="..."
              />
            </div>
            <div class="carousel-item">
              <img
                src="../assets/img/watch4.webp"
                class="d-block w-100"
                alt="..."
              />
            </div>
            <div class="carousel-item">
              <img
                src="../assets/img/watch5.jpeg"
                class="d-block w-100"
                alt="..."
              />
            </div>
          </div>
          <div class="carousel-text">
            The Path to Success <br />
            with Watchlab
          </div>
          <button
            class="carousel-control-next"
            type="button"
            data-bs-target="#carouselExampleControls"
            data-bs-slide="next"
          >
            <span class="">NEXT</span>
            <font-awesome-icon icon="fas fa-angle-right" />
          </button>
        </div>
        <!-- /slider -->
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Hero",
};
</script>

<style lang="scss" scoped>
@import "../style/partials/variables.scss";
@import "../style/app.scss";

@mixin collection-title {
  font-family: "Montserrat-bold";
  font-size: 13px;
  letter-spacing: 2.5px;
}
@mixin button {
  border: 1px solid $bg-logo;
  color: $bg-logo;
  background-color: transparent;
  font-family: $font1;
  font-size: 18px;
  padding: 15px 100px;
  transition: 0.5s;
  margin-top: 50px;
}
@mixin button-hover {
  background-color: $button-color;
  border: 1px solid $button-color;
  color: $basic-color-1;
}

.row > * {
  padding: 0;
}
.container-fluid {
  .row {
    .col {
      .hero {
        background-image: url(../assets/img/hero.jpg);
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;
        min-height: 100vh;
        width: 100%;
        box-shadow: inset 0 0 0 1000px rgba(0, 0, 0, 0.3);
        display: flex;
        justify-content: center;
        align-items: center;
        .text {
          color: $basic-color-1;
          text-align: center;
          h1 {
            font-family: $font1;
            font-size: 9vmin;
            margin: 40px 0;
            word-spacing: 5px;
          }
          h4 {
            @include collection-title;
          }
          h5 {
            font-family: "Montserrat";
            font-size: 12px;
          }
          button {
            @include button;

            &:hover {
              @include button-hover;
            }
          }
        }
      }
      .carousel {
        overflow: hidden;
        width: 380px;
        position: absolute;
        right: 60px;
        bottom: 0;
        border: 1px solid $button-color;
        .carousel-item {
          img {
            height: 250px;
            object-fit: cover;
          }
        }
        .carousel-control-next {
          opacity: 1;
          top: 65%;
          right: 50px;
          font-family: "Montserrat-bold";
          span {
            letter-spacing: 2.5px;
            transition: all 0.5s;
          }
          .fa-angle-right {
            margin-left: 20px;
          }
          &:hover span {
            letter-spacing: 5px;
          }
        }
        .carousel-text {
          position: absolute;
          z-index: 1;
          font-family: $font1;
          top: 30px;
          left: 20px;
          color: $basic-color-1;
          font-size: 23px;
        }
        .carousel-inner::after {
          content: "";
          position: absolute;
          left: 0;
          width: 100%;
          height: 100%;
          z-index: 1;
          background-color: rgba(0, 0, 0, 0.4);
          transition: all 0.5s;
        }
        &:hover .carousel-inner::after {
          background-color: rgba(0, 0, 0, 0.1);
        }
        &:hover .carousel-text {
          text-shadow: 2px 2px 6px rgba(0, 0, 0, 0.91);
        }
      }
    }
  }
}
.hero-container {
  position: relative;
}

$breakpoint-smartphone: 576px;
$breakpoint-ipad: 992px;
@media (max-width: $breakpoint-ipad) {
  .carousel {
    position: absolute;
    left: 50%;
    transform: translate(-50%);
    width: 300px;
    height: 250px;
  }
}
@media (max-width: $breakpoint-smartphone) {
  .hero {
    height: 100vh;
  }
  .carousel {
    display: none;
  }
}
</style>
