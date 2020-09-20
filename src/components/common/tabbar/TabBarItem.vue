<template>

    <div @click="itemClick" class="tab-bar-items">
      <div v-if="!isActive">
        <slot name="item-icon"></slot>
      </div>
      <div v-else>
        <slot name="item-active"></slot>
      </div>
      <div :style="colorCompute">
        <slot name="item-text"></slot>
      </div>
<!--      <img src="../../assets/img/tabbar/主页.png" alt="">-->
<!--      <div>首页</div>-->
    </div>
<!--    <div class="tab-bar-items">-->
<!--      <img src="../../assets/img/tabbar/1.png" alt="">-->
<!--      分类-->
<!--    </div>-->
<!--    <div class="tab-bar-items">-->
<!--      <img src="../../assets/img/tabbar/购物车-23.png" alt="">-->
<!--      购物车-->
<!--    </div>-->
<!--    <div class="tab-bar-items">-->
<!--      <img src="../../assets/img/tabbar/我的.png" alt="">-->
<!--      我的-->
<!--    </div>-->

</template>

<script>
export default {
  name: "TabBarItem",
  props:{
    path:String,
    textColor:{
      type: String,
      default: 'red'
    }
  },
  data(){
    return{
      // isActive: true
    }
  },
  computed:{
    isActive() {
      return this.$route.path.indexOf(this.path) != -1

    },
    colorCompute(){
      return this.isActive ? {color:this.textColor}:{}
    }
  },
  methods:{
    itemClick(){
      this.$router.push(this.path)
    }
  }
}
</script>

<style scoped>
  .tab-bar-items{
    flex: 1;
    text-align: center;
    height: 49px;
    font-size: 14px;
  }
  .tab-bar-items img{
    margin-top: 3px;
    width: 20px;
    height: 20px;
    vertical-align: middle;
  }
  .isClass{
    color: red;
  }
</style>
