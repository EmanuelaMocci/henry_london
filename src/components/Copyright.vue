<template>
  <div class="row">
    <div class="col-12">
      <div class="copywright">
        <div>Copyright Watch/Lab all rights reserved</div>
        <div>website by nssfactory</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Copyright",
};
</script>

<style lang="scss" scoped>
@import "../style/partials/variables.scss";

.copywright {
  background-color: $basic-color-6;
  padding: 30px 80px;
  color: $button-color;
  font-family: $font1;
  display: flex;
  justify-content: space-between;
  font-size: 13px;
  flex-wrap: wrap;
}
</style>
