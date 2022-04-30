<template>
  <div class="main">
    <SectionHistory />
    <SectionTemporaryStore />
    <SectionNewCollection />
    <SectionLabStudio />
    <SectionDiscover />
    <SectionGetInTouch />
  </div>
</template>

<script>
import SectionHistory from "./SectionHistory.vue";
import SectionTemporaryStore from "./SectionTemporaryStore.vue";
import SectionNewCollection from "./SectionNewCollection.vue";
import SectionLabStudio from "./SectionLabStudio.vue";
import SectionDiscover from "./SectionDiscover.vue";
import SectionGetInTouch from "./SectionGetInTouch.vue";

export default {
  name: "Main",
  components: {
    SectionHistory,
    SectionTemporaryStore,
    SectionNewCollection,
    SectionLabStudio,
    SectionDiscover,
    SectionGetInTouch,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/partials/variables.scss";
</style>
