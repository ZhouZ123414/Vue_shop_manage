<template>
 <el-main>
  <!-- 路由占位符 -->
  <router-view></router-view>
 </el-main>
</template>

<script>
 export default {
    name:'homeMain'
}

</script>
<style lang="less" scoped>
.el-main{
    position: relative;
    top: 60px;
  background-color:#eaedf1 ;
}
</style>