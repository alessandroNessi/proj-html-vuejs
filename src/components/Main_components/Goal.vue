<template>
  <div class="goal">
      <div class="content">
          <i :class="this.icon"></i>
          <h4>{{this.header}}</h4>
          <p>{{this.paragraph}}</p>
      </div>
  </div>
</template>

<script>
export default {
  name: "Goal",
  props: {
      icon:String,
      header: String,
      paragraph: String,
  },
  data() {
    return {};
  },
  methods: {},
};
</script>

<style lang="scss" scoped>
@import '../../assets/style/common.scss';
    .goal{
        width: 100%;
        padding:0 10px;
        .content{
            padding: 20px;
            background-color: $grey300;
            i{
                color: $blue400;
                font-size: 40px;
            }
            h4{
                margin: 20px 0;
                font-weight: 600;
            }
            p{
                color: $grey700;
            }
            height: 230px;
            overflow-y: auto;
            &::-webkit-scrollbar{
                width: 0;
            }
        }
    }

</style>
