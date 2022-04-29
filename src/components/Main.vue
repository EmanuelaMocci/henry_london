<template>
  <div class="main">
    <SectionHistory />
    <SectionTemporaryStore />
    <SectionNewCollection />
  </div>
</template>

<script>
import SectionHistory from "./SectionHistory.vue";
import SectionTemporaryStore from "./SectionTemporaryStore.vue";
import SectionNewCollection from "./SectionNewCollection.vue";

export default {
  name: "Main",
  components: {
    SectionHistory,
    SectionTemporaryStore,
    SectionNewCollection,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/partials/variables.scss";
</style>
