<template>
  <main>
    <SectionInvesting />
    <SectionRecent />
    <SectionProud />
    <SectionChoice />
    <SectionCredits />
  </main>
</template>

<script>
import SectionInvesting from "./Main_components/SectionInvesting.vue";
import SectionRecent from "./Main_components/SectionRecent.vue";
import SectionProud from "./Main_components/SectionProud.vue";
import SectionChoice from "./Main_components/SectionChoice.vue";
import SectionCredits from "./Main_components/SectionCredits.vue";

export default {
  name: "Main",
  components: {
    SectionInvesting,
    SectionRecent,
    SectionProud,
    SectionChoice,
    SectionCredits,
  },
  props: {},
  data() {
    return {};
  },
  methods: {},
};
</script>

<style lang="scss" scoped></style>
