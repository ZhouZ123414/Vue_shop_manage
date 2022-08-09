<template>
 <!-- 侧边栏 -->
    <el-aside :width="isCollapse ?'64px':'200px'">
      <div class="toggle-button" @click="toggleCollapse">|||</div>
      <!-- 侧边栏菜单区域 -->
      <el-menu
      :default-active="activePath"
      router
      :collapse-transition="false"
      :collapse = "isCollapse"
      unique-opened
      background-color="#18789e"
      text-color="#fff"
      active-text-color="#409eff">
      <!-- 一级菜单 -->
      <el-submenu :index="item.id + ''" v-for="item in menuList" :key="item.id">
        <!-- 一级菜单模板区域 -->
        <template slot="title">
          <!-- 图标 -->
          <i :class="iconsObj[item.id]"></i>
          <!-- 文本 -->
          <span>{{item.authName}}</span>
        </template>
        <!-- 二级菜单 -->
        <el-menu-item 
          @click="saveNavState('/' + subItem.path)"
         :index="'/' + subItem.path" v-for="subItem in item.children" :key="subItem.id">
          <template slot="title">
          <!-- 图标 -->
          <i class="el-icon-menu"></i>
          <!-- 文本 -->
          <span>{{subItem.authName}}</span>
        </template>
        </el-menu-item>
      </el-submenu>
    </el-menu>
    </el-aside>
</template>

<script>
 export default {
    name:'homeSide',
    data() {
        return {
            // 左侧菜单
            menuList: [],
            iconsObj: {
                "125": "iconfont icon-user",
                "103": "iconfont icon-tijikongjian",
                "101": "iconfont icon-shangpin",
                "102": "iconfont icon-danju",
                "145": "iconfont icon-baobiao"
            },
            // 是否折叠
            isCollapse: false,
            // 被激活的链接地址
            activePath:''
        };
    },
    created() {
        this.getMenuList();
        this.activePath = window.sessionStorage.getItem('activePath')
    },
    methods: {
        // 获取所有菜单
        async getMenuList() {
            const { data: res } = await this.$http.get("menus");
            if (res.meta.status !== 200)
                return this.$message.error(res.meta.msg);
            this.menuList = res.data;
        },
        // 点击按钮，切换菜单的折叠与展开
        toggleCollapse() {
            this.isCollapse = !this.isCollapse;
        },
        // 保存链接的激活状态
        saveNavState(activePath){
          window.sessionStorage.setItem('activePath',activePath)
          this.activePath = activePath
        },
    },
}

</script>
<style lang="less" scoped>
.el-aside{
    position: relative;
    top: 60px;
  background: linear-gradient(to top, rgb(21, 172, 232), rgb(24, 118, 155),rgb(5, 67, 91));
  .el-menu{
    border-right: none;
  }
}
.iconfont{
  margin-right: 10px;
}
.toggle-button{
  background-color: #4a5064;
  font-size: 10px;
  line-height: 24px;
  color: #fff;
  text-align: center;
  letter-spacing: 0.2em;
  cursor: pointer;
}
</style>