<template>
  <div>
    <tabbar>
      <tabbar-item path="/home" activesColor="deeppink">
        <img slot="item-icon" src="~assets/img/tabbar/home.svg">
        <img slot="item-icon-active" src="~assets/img/tabbar/home_active.svg">
        <div slot="item-text">首页</div>
      </tabbar-item>
      <tabbar-item path="/category" activesColor="deeppink">
        <img slot="item-icon" src="~assets/img/tabbar/category.svg">
        <img slot="item-icon-active" src="~assets/img/tabbar/category_active.svg">
        <div slot="item-text">分类</div>
      </tabbar-item>
      <tabbar-item path="/shopcart" activesColor="deeppink">
        <img slot="item-icon" src="~assets/img/tabbar/shopcart.svg">
        <img slot="item-icon-active" src="~assets/img/tabbar/shopcart_active.svg">
        <div slot="item-text">购物车</div>
      </tabbar-item>
      <tabbar-item path="/profile" activesColor="deeppink">
        <img slot="item-icon" src="~assets/img/tabbar/profile.svg">
        <img slot="item-icon-active" src="~assets/img/tabbar/profile_active.svg">
        <div slot="item-text">我的</div>
      </tabbar-item>
    </tabbar>
  </div>
</template>

<script>
import tabbar from "components/common/tabbar/Tabbar";
import tabbarItem from "components/common/tabbar/TabbarItem";
export default {
  name:'mainTabbar',
  components: { tabbar,tabbarItem }
}
</script>
  
<style scope>
  
</style>