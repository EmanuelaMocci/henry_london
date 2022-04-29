<template>
  <div class="main">
    <SectionHistory />
  </div>
</template>

<script>
import SectionHistory from "./SectionHistory.vue";

export default {
  name: "Main",
  components: {
    SectionHistory,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/partials/variables.scss";
</style>
