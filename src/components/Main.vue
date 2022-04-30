<template>
  <div class="main">
    <SectionHistory />
    <SectionTemporaryStore />
    <SectionNewCollection />
    <SectionLabStudio />
    <SectionDiscover />
  </div>
</template>

<script>
import SectionHistory from "./SectionHistory.vue";
import SectionTemporaryStore from "./SectionTemporaryStore.vue";
import SectionNewCollection from "./SectionNewCollection.vue";
import SectionLabStudio from "./SectionLabStudio.vue";
import SectionDiscover from "./SectionDiscover.vue";

export default {
  name: "Main",
  components: {
    SectionHistory,
    SectionTemporaryStore,
    SectionNewCollection,
    SectionLabStudio,
    SectionDiscover,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/partials/variables.scss";
</style>
