<!--  -->
<template>
  <div class="textt">
    <div class="content">
      <div class="tops">
        <div class="tags active">补充协议1</div>
        <div class="tags">补充协议1</div>
        <div class="tags">补充协议1</div>
      </div>
      <el-button type="primary" size="mini" class="add">新增</el-button>
      <div class="block">
        <div>协议内容</div>
        <div class="delete">删除</div>
        <div class="agreement"></div>
      </div>
    </div>
  </div>
</template>

<script>
//这里可以导入其他文件（比如：组件，工具js，第三方插件js，json文件，图片文件等等）
//例如：import 《组件名称》 from '《组件路径》';

export default {
  //import引入的组件需要注入到对象中才能使用
  components: {},
  data() {
    //这里存放数据
    return {};
  },
  //监听属性 类似于data概念
  computed: {},
  //监控data中的数据变化
  watch: {},
  //方法集合
  methods: {},
  beforeCreate() {}, //生命周期 - 创建之前
  //生命周期 - 创建完成（可以访问当前this实例）
  created() {},
  beforeMount() {}, //生命周期 - 挂载之前
  //生命周期 - 挂载完成（可以访问DOM元素）
  mounted() {},
  beforeUpdate() {}, //生命周期 - 更新之前
  updated() {}, //生命周期 - 更新之后
  beforeDestroy() {}, //生命周期 - 销毁之前
  destroyed() {}, //生命周期 - 销毁完成
  activated() {}, //如果页面有keep-alive缓存功能，这个函数会触发
};
</script>
<style lang="less" scoped>
.textt {
  //   background-color: #fff;
  margin-top: 10px;
  padding: 15px 0px;
  .content {
    position: relative;
    .tops {
      width: 100%;
      height: 42px;
      .tags {
        width: 114px;
    height: 36px;
    text-align: center;
    line-height: 36px;
    float: left;
    color: #b6b6b6;
    border: 1px solid #ccc;
    background-color: #fff;
      }
      .active {
        color: #2998fe;
        font-weight: bold;
      }
    }
    .el-button {
      font-size: 15px;
      position: absolute;
      top: -3px;
      right: 0px;
      width: 65px;
    }
    .block {
      width: calc(100% - 40px);
      border: 1px solid #ccc;
      height: 150px;
      position: relative;
      top: -5px;
      padding: 10px 20px;
      background-color: #fff;
      color: #505050;
      .agreement {
        margin-top: 10px;
        width: calc(100% - 40px);
        height: 70%;
        background-color: #f5f5f5;
        border: 1px solid #ccc;
      }
      .delete {
        width: 60px;
        height: 25px;
        color: #fea428;
        border: 1px solid #ccc;
        position: absolute;
        top: 5px;
        right: 5px;
        text-align: center;
        line-height: 25px;
        border-radius: 5px;
      }
    }
  }
}
</style>