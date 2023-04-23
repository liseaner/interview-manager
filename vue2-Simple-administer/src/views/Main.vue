<template>
  <div>
    <el-container>
      <el-aside width="auto">
        <common-aside />
      </el-aside>
      <el-container class="right">
        <el-header>
          <common-header />
        </el-header>
        <common-tag />
        <el-main>
          <router-view></router-view>
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script>
import CommonAside from "../components/CommonAside.vue";
import CommonHeader from "../components/CommonHeader.vue";
import CommonTag from "../components/CommonTag.vue";
export default {
  data() {
    return {};
  },
  components: {
    CommonAside,
    CommonHeader,
    CommonTag,
  },
};
</script>

<style lang="less" scoped>
.el-header {
  padding: 0;
}
.el-container {
  height: 100vh;
  .el-main {
  background-color: #f5f5f5;
 padding: 0 !important;
  /* margin: 0; */
}
}


</style>