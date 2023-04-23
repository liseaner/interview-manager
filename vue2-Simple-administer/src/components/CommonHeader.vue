<template>
  <div class="header-container">
    <div class="l-content">
      <div
        style="margin-right: 20px"
        @click="handleMenu"
        size="mini"
        font-size="32px"
        class="button"
      >
        <i class="el-icon-s-home"></i>
      </div>
      <span>首页</span>
    </div>
    <div class="l-content">
      <div
        style="margin-right: 20px"
        @click="handleMenu"
        size="mini"
        font-size="32px"
        class="button"
      >
        <i class="el-icon-s-home"></i>
      </div>
      <span>首页</span>
    </div>
    <div class="l-content">
      <div
        style="margin-right: 20px"
        @click="handleMenu"
        size="mini"
        font-size="32px"
        class="button"
      >
        <i class="el-icon-s-home"></i>
      </div>
      <span>辖区管理</span>
    </div>
    <div class="l-content adv">
      <div class="adv-icon">销讯通</div>
    </div>
  </div>
</template>
  <script>
import { mapState } from "vuex";
import Cookie from "js-cookie";
export default {
  data() {
    return {};
  },
  components: {},
  methods: {
    handleMenu() {
      this.$store.commit("collapseMenu");
    },
    handleClick(command) {
      if (command == "cancel") {
        // 清除cookie中的token
        Cookie.remove("token");
        // 清除cookie中的menu
        Cookie.remove("menu");
        // 跳转到登录uy
        this.$router.push("/login");
      }
    },
  },
  computed: {
    ...mapState({
      tags: (state) => state.tab.tabsList,
    }),
  },
  mounted() {
    console.log("tags", this.tags);
  },
};
</script>
  
  <style lang="less">
.header-container {
  padding: 0 20px;
  background-color: #2a3139;
  height: 60px;
  display: flex;
  // justify-content: space-between;
  align-items: center;
  color: #aaacae;
  .text {
    color: #fff;
    font-size: 14px;
    margin-left: 10px;
  }
  .r-content {
    .user {
      width: 40px;
      height: 40px;
      border-radius: 50%;
    }
  }
  .l-content {
    display: flex;
    align-items: center;
    margin-left: 26px;
    .button {
      background-color: #51565c;
      border: 0px;
      color: #bbbbbb;
      width: 45px;
      height: 40px;
      text-align: center;
      line-height: 40px;
      border-radius: 11px;

      .el-icon-s-home {
        font-size: 21px;
      }
    }
    span {
      margin: 0 20px 0 -10px;
    }
    .el-breadcrumb__item {
      /deep/.el-breadcrumb__inner {
        //没有data-唯一标识所以用/deep/样式的穿刺
        font-weight: normal;
        &.is-link {
          //&表示有el-breadcrumb__inner又有is-link
          color: #666;
        }
      }
    }
    &:last-child {
      .el-breadcrumb inner {
        color: #fff;
      }
    }
  }
  .adv {
    .adv-icon {
      background-color: #fff;
      width: 100px;
      height: 50px;
      text-align: center;
      line-height: 50px;
    }
  }
}
</style>

<!-- <style lang="less">
.el-button {
  .el-icon-s-home {
    font-size: 16px;
  }
}
</style> -->