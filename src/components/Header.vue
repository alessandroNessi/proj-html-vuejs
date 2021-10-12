<template>
  <header ref="header">
    <div class="container-l">
      <a href="#"
        ><img src="../assets/img/MasterStudy_logo.svg" alt="MasterStudy logo"
      /></a>
      <a href="#"
        ><h3 class="grey subtitle"><i class="fas fa-bars"></i> CATEGORY</h3></a
      >
      <div class="grow">
        <input
          placeholder="Search Courses"
          class="search"
          type="text"
        /><button><i class="fas fa-search"></i></button>
      </div>
      <a class="grey subtitle"
        ><i class="blue fas fa-bullhorn"></i> Become an Instructor</a
      >
      <a class="grey subtitle"
        ><i class="blue fas fa-briefcase"></i> For Enterprise</a
      >
      <a class="subtitle blue"
        ><i class="blue far fa-user"></i><span class="blue"> Log In</span></a
      >
      <button class="rounded"><h4>SIGN UP</h4></button>
      <a href="#"><i class="blue far fa-bookmark"></i></a>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: {
    headerHeight: String,
  },
  data() {
    return {};
  },
  methods: {},
  mounted() {
    this.$refs.header.style.height = this.headerHeight;
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/common.scss";
.container-l {
  font-size: 14px;
  display: flex;
  justify-content: space-between;
}
.grow {
  flex-grow: 0.75;
}
.grey {
  color: $grey900;
}
.blue {
  color: $blue400;
}
.search {
  background-color: $grey300;
  width: 90%;
  padding-left: 10px;
}
</style>
