<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col">
        <div class="hero">
          <div class="text">
            <h4>LONDON COLLECTION SEASON</h4>
            <h1>
              New Selection Of <br />
              Henry London
            </h1>
            <h5>An estimable experience in the modern collection house</h5>
          </div>
        </div>
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
        height: 90vh;
        width: 100%;
        box-shadow: inset 0 0 0 1000px rgba(0, 0, 0, 0.4);
        display: flex;
        justify-content: center;
        align-items: center;
        .text {
          color: white;
          text-align: center;
          margin: 0 20px;
          h1 {
            font-family: "Miller";
            font-size: 60px;
            margin: 40px 0;
            word-spacing: 5px;
          }
          h4 {
            font-family: "Montserrat-bold";
            font-size: 13px;
            letter-spacing: 2.5px;
          }
          h5 {
            font-family: "Montserrat";
            font-size: 12px;
          }
        }
      }
    }
  }
}
</style>
