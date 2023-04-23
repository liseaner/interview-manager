<template>
  <div class="tabs">
    <!-- 面包屑 -->
    <el-breadcrumb separator="/">
      <el-breadcrumb-item
        v-for="item in tags"
        :key="item.path"
        :to="{ path: item.path }" style=" color: #a9a9a9;"
        >{{ item.label }}</el-breadcrumb-item
      >
      <!-- {{ item.label }} -->
    </el-breadcrumb>
    <div class="page">{{this.$route.meta }}</div>
  </div>
</template>

<script>
import { mapState, mapMutations } from "vuex";
export default {
  name: "CommonTag",
  data() {
    return {
      name:""
    };
  },
  computed: {
    ...mapState({
      tags: (state) => state.tab.tabsList,
    }),
    // route: JSON.parse(localStorage.getItem("route")),
  },
  methods: {
    ...mapMutations(["closeTag"]),
    // 点击tag跳转的功能
    changeMenu(item) {
      console.log(item);
      this.$router.push({ name: item.name });
    },
    // 点击tag删除的功能
    handleClose(item, index) {
      // 调用store中的mutation
      this.closeTag(item);
      const length = this.tags.length;
      // 删除之前的跳转逻辑
      if (item.name !== this.$route.name) {
        return;
      }
      // 表示删除的最后一项
      if (index === length) {
        this.$router.push({
          name: thid.tags[index - 1].name,
        });
      } else {
        this.$router.push({
          name: this.tags[index].name,
        });
      }
    },
  },
  created() {
    // console.log("this.route", this.$route);
    // var storage=window.localStorage;
    // console.log("route", JSON.parse(storage.getItem("route")));
  },
};
</script>

<style lang="less" scoped>
.tabs {
  padding: 20px 20px 10px 20px;

  .el-tag {
    margin-right: 15px;
    cursor: pointer;
  }
}
.page{
  font-size: 18px;
  margin-top: 10px;
}
</style>