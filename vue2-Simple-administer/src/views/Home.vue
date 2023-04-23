<template>
<el-scrollbar>
  <div class="content">
    <div class="first">
      <img src="../../src/assets/images/Snipaste_2023-04-22_18-04-24.png" />
      <cart-main />
    </div>
    <div class="second">
      <img src="../../src/assets/images/Snipaste_2023-04-22_18-05-22.png" />
      <product-content />
    </div>
    <div class="footer">
      <img src="../../src/assets/images/Snipaste_2023-04-22_18-05-39.png" />
      <supply-content />
    </div>
    <div class="last">
      <el-button type="primary" size="medium">保存</el-button>
    </div>
  </div>
</el-scrollbar>
</template>

<script>
import CartMain from "@/components/CartMain.vue";
import ProductContent from "@/components/ProductContent.vue";
import SupplyContent from "@/components/SupplyContent.vue";
export default {
  data() {
    return {};
  },
  mounted() {},
  components: {
    CartMain,
    ProductContent,
    SupplyContent,
  },
};
</script>

<style lang="less" scoped>

  .content {
  background-color: #f5f5f5;
  height: 100%;
  .first {
    // border-top: 2px dotted #ccc;
    // width: calc(100% - 20px);
    // // height: 40%;
    // position: relative;
    border-top: 2px dotted #ccc;
    /* width: calc(100% - 20px); */
    position: relative;
    margin: 20px;
    img {
      position: absolute;
      top: -22px;
      left: 50%;
      margin-left: -86px;
    }
  }
  .second {
    border-top: 2px dotted #ccc;
    /* width: calc(100% - 20px); */
    position: relative;
    margin: 20px;
    img {
      position: absolute;
      top: -22px;
      left: 50%;
      margin-left: -86px;
    }
  }
  .footer {
    border-top: 2px dotted #ccc;
    /* width: calc(100% - 20px); */
    position: relative;
    // margin: 20px;
    margin: 20px 20px 5px 20px;
    img {
      position: absolute;
      top: -22px;
      left: 50%;
      margin-left: -86px;
    }
   
  }
  .last {
    width: 100%;
    height: 43px;
    background-color: #fff;
    // padding: 14px 20px;
    text-indent: 2em;
    }
}



</style>