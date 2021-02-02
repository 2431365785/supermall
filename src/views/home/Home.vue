<template>
  <div>
    <!-- 顶部 -->
    <nav-bar class="home-nav">
      <div slot="center">购物街</div>
    </nav-bar>

    <!-- 轮播图 -->
    <swiper :list="banners" />

  </div>
</template>

<script>
import NavBar from 'components/common/navbar/NavBar'

import { getHomeMultidata } from 'network/home'

export default {
  name: 'Home',
  data() {
    return {
      banners: [],
      recommends: [],
    }
  },
  created() {
    this.getHomeMultidata()
  },
  methods: {
    /* 网络请求相关 */
    // 获取轮播图等数据
    getHomeMultidata() {
      getHomeMultidata().then((res) => {
        console.log(res)
        this.banners = res.data.banner.list
        this.recommends = res.data.recommend.list
      })
    },
  },
  components: {
    NavBar,
  },
}
</script>

<style  scoped>
.home-nav {
  background-color: var(--color-tint);
  color: white;
}
</style>
