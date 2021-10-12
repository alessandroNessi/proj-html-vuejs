<template>
  <main>
    <SectionInvesting />
    <SectionRecent/>
  </main>
</template>

<script>
import SectionInvesting from "./Main_components/SectionInvesting.vue";
import SectionRecent from "./Main_components/SectionRecent.vue"
export default {
  name: "Main",
  components: {
    SectionInvesting,
    SectionRecent,
  },
  props: {},
  data() {
    return {};
  },
  methods: {},
};
</script>

<style lang="scss" scoped></style>
