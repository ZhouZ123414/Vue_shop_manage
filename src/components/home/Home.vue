<template>
  <el-container class="homeContainer">
    <!-- 头部区域 -->
    <HomeHeader />
    <!-- 页面主体区域 -->
    <el-container>
      <HomeSide />
      <!-- 右侧内容 -->
      <HomeMain />
    </el-container>
  </el-container>
</template>

<script>
import HomeHeader from './homeHeader.vue'
import HomeSide from './homeSide.vue'
import HomeMain from './homeMain.vue'
export default {
  name: 'Home',
  components: { HomeHeader, HomeSide, HomeMain },
}
</script>
<style lang="less" scoped>
.homeContainer {
  height: 100%;
}
</style>
