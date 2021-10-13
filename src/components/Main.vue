<template>
  <main>
    <SectionInvesting />
    <SectionRecent/>
    <SectionProud/>
  </main>
</template>

<script>
import SectionInvesting from "./Main_components/SectionInvesting.vue";
import SectionRecent from "./Main_components/SectionRecent.vue";
import SectionProud from "./Main_components/SectionProud.vue";
export default {
  name: "Main",
  components: {
    SectionInvesting,
    SectionRecent,
    SectionProud,
  },
  props: {},
  data() {
    return {};
  },
  methods: {},
};
</script>

<style lang="scss" scoped></style>
