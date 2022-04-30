<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-sm-12 col-md-6 image-container">
        <div class="image">
          <img src="../assets/img/groom.jpg" alt="" />
        </div>
        <div class="text">
          <h4>INSTAGRAM</h4>
          <h2>
            Discover <br />
            Watch Lab
          </h2>
        </div>
      </div>
      <div class="col-sm-12 col-md-6 container-img mt-4 mt-md-0">
        <div class="row g-0 row-cols-2">
          <div class="col-6">
            <img src="../assets/img/london2.jpg" alt="" />
          </div>
          <div class="col-6">
            <img src="../assets/img/watch-grid.jpeg" alt="" />
          </div>
          <div class="col-6">
            <img src="../assets/img/love.jpeg" alt="" />
          </div>
          <div class="col-6">
            <img src="../assets/img/watch-grid5.gif" alt="" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionDiscover",
};
</script>

<style lang="scss" scoped>
@import "../style/partials/variables.scss";

@mixin centered {
  max-width: 85%;
  margin: auto;
}
@mixin collection-title {
  font-family: "Montserrat-bold";
  font-size: 13px;
  letter-spacing: 2.5px;
}
.row > * {
  padding: 0;
}
.container-fluid {
  @include centered;
}
img {
  width: 100%;
  min-height: 100%;
  object-fit: cover;
}
.image::after {
  content: "";
  position: absolute;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
  background-color: rgba(0, 0, 0, 0.4);
}
.image-container {
  position: relative;
}
.text {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  color: white;
  z-index: 1;
}
h4 {
  @include collection-title;
}
h2 {
  font-family: $font1;
  font-size: 9vmin;
}
</style>
