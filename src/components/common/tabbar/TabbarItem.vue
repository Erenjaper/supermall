<template>
  <div class="tabbarItem" @click="itemClick">
    <div v-if="!isActives"><slot name="item-icon"></slot></div>
    <div v-else><slot name="item-icon-active"></slot></div>
    <div :style="isActivesColor"><slot name="item-text"></slot></div>
  </div>
</template>

<script>
export default {
  name: "tabbarItem",
  props:{
    path:String,
    activesColor:{
      type:String,
      default:'red'
    }
  },
  computed:{
    isActives(){
      return this.$route.path.indexOf(this.path) !== -1 
    },
    isActivesColor(){
      return this.isActives ? {color:this.activesColor}:{}
    }
  },
  methods:{
    itemClick(){
      this.$router.replace(this.path);
    }
  }
};
</script>
  
<style scope>
.tabbarItem {
  flex: 1;
  display: inline-block;
  height: 49px;
  text-align: center;
  font-size: 12px;
}
.tabbarItem img{
  margin-top: 3px;
  height: 24px;
  width: 24px;
  vertical-align: middle;
  margin-bottom: 2px;
}
</style>