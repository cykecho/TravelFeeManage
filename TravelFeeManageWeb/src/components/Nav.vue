<template>
    <!-- 导航栏 -->
    <div class="container">
        <el-menu
        router
        :default-active="$route.path"
        class="el-menu"
        mode="horizontal"
        @select="handleSelect"
        background-color="#70a1ff"
        text-color="#fff"
        active-text-color="#862e9c">
            <el-menu-item index="/travel" style="margin-left: 60px">旅游管理</el-menu-item>
            <el-menu-item index="/postal">邮政编码</el-menu-item>
            <el-menu-item index="/train">火车时刻</el-menu-item>
            <el-menu-item index="/phone">号码归属</el-menu-item>
            <!-- 个人中心 -->
            <a href="javascript:void(0)"><el-avatar class="el-avatar" src="https://cube.elemecdn.com/0/88/03b0d39583f48206768a7534e55bcpng.png"></el-avatar></a>
        </el-menu>
        <router-view></router-view>
    </div>
</template>
<script>
export default {
  data () {
    return {
      activeIndex: ''
    }
  },
  methods: {
    handleSelect (key, keyPath) {
      console.log(key, keyPath)
    }
  }
}
</script>
<style lang="less" scoped>
.container{
  height: 100%;
  width: 100%;
  .el-avatar{
      float: right;
      margin: 10px 60px 0 0;
  }
}

</style>
