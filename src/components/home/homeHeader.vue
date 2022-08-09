<template>
 <el-header>
    <div>
      <img src="../../assets/youcheng.png" alt="">
      <span>柚城后台管理系统</span>
    </div>
    <el-button type="info" @click="logout">退出登录</el-button>
  </el-header>
</template>

<script>
 export default {
    name:'homeHeader',
    methods:{
        logout() {
            window.sessionStorage.clear();
            this.$router.push("/login");
        },
    }
}

</script>
<style lang="less" scoped>
.el-header{
    min-width: 1366px;
    position: absolute;
    background: linear-gradient(to left, rgb(21, 172, 232), rgb(24, 118, 155),rgb(5, 67, 91));
    display: flex;
    justify-content: space-between;
    padding-left:0 ;
    align-items: center;
    color: #fff;
    font-size: 20px;
    width: 100%;
    div {
        display: flex;
        align-items:center;
        span{
        margin-left: 15px;
        }
        img{
            height: 60px;
            width: 60px;
            border-radius: 50%;
        }
    }
}
.el-button{
    background-color: blue;
}
</style>