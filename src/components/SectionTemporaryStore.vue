<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-xs-12 col-lg-6 left-text">
        <h4>LONDON COLLECTION SEASON</h4>
        <h2>Temporary Store</h2>
        <p>
          On the other hand, we denounce with righteous indignation and dislike
          men who are so beguiled and demoralized by the charms of pleasure of
          the moment so blinded by desire
        </p>
        <button>View</button>
      </div>
      <div class="col-xs-12 col-lg-6 d-flex justify-content-end">
        <div class="image">
          <img
            src="../assets/img/store.jpg"
            alt="Top part of a
            skyscraper white clean lightblue sky"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionTemporaryStore",
};
</script>

<style lang="scss" scoped>
@import "../style/partials/variables.scss";

@mixin centered {
  max-width: 85%;
  margin: auto;
}
@mixin collection-title {
  font-family: $font3;
  font-size: 13px;
  letter-spacing: 2.5px;
}
@mixin description {
  color: $basic-color-3;
  font-family: $font2;
  letter-spacing: 0.5px;
  font-size: 14px;
  line-height: 30px;
  width: 60%;
  padding-top: 60px;
}
@mixin button {
  border: 1px solid $bg-logo;
  color: $bg-logo;
  background-color: transparent;
  font-family: $font1;
  font-size: 18px;
  padding: 15px 100px;
  transition: 0.5s;
  margin: 50px 0 30px 0;
}
@mixin button-hover {
  background-color: $button-color;
  border: 1px solid $button-color;
  color: $basic-color-1;
}
@mixin centered-text {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.container-fluid {
  text-align: center;
  @include centered;

  h4 {
    @include collection-title;
  }
  h2 {
    font-family: $font1;
    padding-top: 20px;
  }
  p {
    @include description;
  }
  button {
    @include button;
    &:hover {
      @include button-hover;
    }
  }
  img {
    width: 100%;
  }
}
.row > * {
  padding: 0;
}
.left-text {
  @include centered-text;
  padding-top: 30px;
}
</style>
