<template>
  <!-- 100vh表示侧边栏延伸到底部 -->
  <el-container style="height: 100vh; border: 1px solid #eee">
    <el-aside width="200px" style="background-color: rgb(238, 241, 246)">
      <!-- 添加路由，实现类似超链接的功能 -->
      <el-menu router :default-openeds="['1']">
        <el-submenu index="1">
          <template slot="title"
            ><i class="el-icon-tickets"></i>内容管理</template
          >
          <el-menu-item index="/articles/create">新建内容</el-menu-item>
          <el-menu-item index="/articles/index">文章列表</el-menu-item>
        </el-submenu>
      </el-menu>
    </el-aside>

    <el-container>
      <el-header style="text-align: right; font-size: 12px">
        <el-dropdown>
          <i class="el-icon-setting" style="margin-right: 15px"></i>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item>查看</el-dropdown-item>
            <el-dropdown-item>新增</el-dropdown-item>
            <el-dropdown-item>删除</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
        <span>王小虎</span>
      </el-header>

      <el-main>
        <!-- 放入组件内容 -->
        <router-view></router-view>
      </el-main>
    </el-container>
  </el-container>
</template>

<style>
html,
body {
  padding: 0;
  margin: 0;
}

.el-header {
  background-color: #b3c0d1;
  color: #333;
  line-height: 60px;
}

.el-aside {
  color: #333;
}
</style>
