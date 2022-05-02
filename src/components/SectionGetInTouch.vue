<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col">
        <h2>Get in Touch</h2>
        <h4>
          DISCOVER MORE ABOUT NEWS, <br />
          EXCLUSIVE EVENTS AND DISCOUNT
        </h4>
        <div class="input">
          <input type="text" name="text" placeholder="type your email" />
          <button>ok</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionGetInTouch",
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
@mixin centered-text {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.container-fluid {
  @include centered;
  @include centered-text;
  color: $basic-color-1;
  text-align: center;
  margin-top: 50px;
  background-image: url(../assets/img/desk2.jpg);
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  height: 260px;
  box-shadow: inset 0 0 0 1000px rgba(209, 188, 156, 0.7);
  h2 {
    font-family: $font1;
    font-size: 9vmin;
  }
  h4 {
    @include collection-title;
    margin-bottom: 25px;
  }
  .input {
    width: 100%;
    display: flex;
    justify-content: space-between;
    input {
      background: transparent;
      border: 1px solid $basic-color-1;
      padding: 10px 15px;
      width: 85%;
      outline: none;
      color: $basic-color-1;
    }
    ::placeholder {
      color: $basic-color-1;
      font-family: $font1;
    }
    button {
      border: 1px solid $basic-color-1;
      background: transparent;
      color: $basic-color-1;
      padding: 10px 15px;
    }
  }
}
</style>
