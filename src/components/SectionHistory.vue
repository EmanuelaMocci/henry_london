<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-12">
        <h2
          data-aos="fade-down"
          data-aos-duration="1500"
          data-aos-delay="500"
          data-aos-once="true"
        >
          History and <br />
          Patriarcal season
        </h2>
      </div>

      <div
        class="row justify-content-between"
        data-aos="fade-down"
        data-aos-duration="1500"
        data-aos-delay="600"
        data-aos-once="true"
      >
        <div class="col-12 col-md-6 col-lg-5">
          <p>
            On the other hand, we denounce with righteous indignation and
            dislike men who are beguiled and demoralized by the charms of
            pleasure of the moment, so blinded by desire
          </p>
        </div>
        <div class="col-12 col-md-6 col-lg-6">
          <p>
            But I must explain to you how all this mistaken idea of denouncing
            pleasure and praising pain was born and I will give you a complete
            account of the system, and expund the actual teachings of the great
            explorer of the truth, the master-builder of human happiness. No
            that are extremely painful
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionHistory",
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
.container-fluid {
  font-family: $font1;
  @include centered;
  padding: 40px 0;

  h2 {
    font-size: 9vmin;
    padding-bottom: 40px;
  }

  p {
    @include description;
    padding-left: 10px;
  }
}
.row > * {
  padding: 0;
}
</style>
