<template>
  <div>
    <tab-bar>
      <tab-bar-item path="/home">
        <img
          slot="item-icon"
          src="~assets/img/tabbar/home.png"
          alt=""
        />
        <img
          slot="item-icon-active"
          src="~assets/img/tabbar/home_active.png"
          alt=""
        />
        <div slot="item-text">首页</div>
      </tab-bar-item>
      <tab-bar-item path="/classify">
        <img
          slot="item-icon"
          src="~assets/img/tabbar/classify.png"
          alt=""
        />
        <img
          slot="item-icon-active"
          src="~assets/img/tabbar/classify_active.png"
          alt=""
        />
        <div slot="item-text">分类</div>
      </tab-bar-item>
      <tab-bar-item path="/cart">
        <img
          slot="item-icon"
          src="~assets/img/tabbar/shoppingCar.png"
          alt=""
        />
        <img
          slot="item-icon-active"
          src="~assets/img/tabbar/shoppingCar_active.png"
          alt=""
        />
        <div slot="item-text">购物车</div>
      </tab-bar-item>
      <tab-bar-item path="/profile">
        <img
          slot="item-icon"
          src="~assets/img/tabbar/profile.png"
          alt=""
        />
        <img
          slot="item-icon-active"
          src="~assets/img/tabbar/profile_active.png"
          alt=""
        />
        <div slot="item-text">我的</div>
      </tab-bar-item>
    </tab-bar>
  </div>
</template>

<script>
import TabBar from 'components/common/tabbar/TabBar'
import TabBarItem from 'components/common/tabbar/TabBarItem'

export default {
  name: 'MainTabbar',
  data () {
    return {
    }
  },
  components: {
    TabBar,
    TabBarItem,
  },
}
</script>

<style scoped>

</style>