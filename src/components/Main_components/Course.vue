<template>
  <div :class="this.preview?`col-8`:this.lateral?`col-12`:`col-4`" class="course">
      <img :src="require(`../../assets/img/${this.img}`)" :alt="this.header">
      <div class="course_details" >
          <h4>{{this.header}}</h4>
          <p>{{this.paragraph}} corsi</p>
      </div>
  </div>
</template>

<script>
export default {
  name: "Course",
  props: {
      img: String,
      header: String,
      paragraph: String,
      preview: Boolean,
      lateral: Boolean
  },
  data() {
    return {};
  },
  methods: {},
};
</script>

<style lang="scss" scoped>
@import '../../assets/style/common.scss';
    .course{
        
        padding: 10px 15px;
        overflow: hidden;
        width: 100%;
        .course_details{
            display: flex;
            justify-content: space-between;
            h4{
                font-weight: 600;
            }
        }
        img{
            width: 100%;
            margin-bottom: 5px;
        }
    }
</style>
