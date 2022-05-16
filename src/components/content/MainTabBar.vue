<template>
  <tab-bar>
      <tab-bar-item path="/home" >
        <template v-slot:item-icon>
          <img src="~assets/img/tabbar/3.png">
        </template>
        <template v-slot:item-icon-active>
          <img slot="item-icon-active" src="~assets/img/tabbar/2.jpg">
        </template>
        <template v-slot:item-text>
          <div>首页</div>
        </template>
      </tab-bar-item>
      <tab-bar-item  path="/category" activeColor="blue">
        <template v-slot:item-icon>
          <img src="~assets/img/tabbar/4.png">
        </template>
        <template v-slot:item-icon-active>
          <img slot="item-icon-active" src="~assets/img/tabbar/2.jpg">
        </template>
        <template v-slot:item-text>
          <div>分类</div>
        </template>
      </tab-bar-item>
      <tab-bar-item path="/cart" activeColor="blue">
        <template v-slot:item-icon>
          <img src="~assets/img/tabbar/5.png">
        </template>
        <template v-slot:item-icon-active>
          <img slot="item-icon-active" src="~assets/img/tabbar/2.jpg">
        </template>
        <template v-slot:item-text>
          <div>购物车</div>
        </template>
      </tab-bar-item>
      <tab-bar-item path="/profile" activeColor="blue">
        <template v-slot:item-icon>
          <img src="~assets/img/tabbar/6.png">
        </template>
        <template v-slot:item-icon-active>
          <img slot="item-icon-active" src="~assets/img/tabbar/2.jpg">
        </template>
        <template v-slot:item-text>
          <div>我的</div>
        </template>
      </tab-bar-item>
    </tab-bar>
</template>

<script>
import TabBar from  'components/common/tabbar/TabBar'
import TabBarItem from 'components/common/tabbar/TabBarItem'
export default {
  name: 'MainTabBar',
  components: {
    TabBar,
    TabBarItem
  }
}
</script>

<style>

</style>