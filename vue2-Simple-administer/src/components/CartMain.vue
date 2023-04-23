<!--  -->
<template>
  <div>
    <el-form
      :model="ruleForm"
      :rules="rules"
      ref="ruleForm"
      label-width="100px"
      class="demo-ruleForm top_form "
    >
      <el-row>
        <el-col :span="12">
          <el-form-item label="协议客户：" prop="name" size="small">
            <el-input
              v-model="ruleForm.name"
              placeholder="选择客户"
              style="width: 100px"
              size="small"
            ></el-input>
            <!-- <el-input v-model="input" placeholder="请输入内容"></el-input> -->
            <span style="margin-left: 15px">上海正也公司</span>
          </el-form-item>
        </el-col>
        <el-col :span="12">
          <el-form-item label="协议状态：" prop="status" class="modify">
            <el-select
              style="width: 200px; height: 32px"
              v-model="ruleForm.status"
              placeholder="正常"
            >
              <el-option label="1" value="shanghai"></el-option>
              <el-option label="2" value="beijing"></el-option>
            </el-select> </el-form-item
        ></el-col>
      </el-row>
      <el-row>
        <el-col :span="12">
          <el-form-item class="line" label="购进指标：" prop="index">
            <el-select
              v-model="ruleForm.index"
              placeholder="金额"
              style="width: 100px" 
            >
              <el-option label="区域一" value="shanghai"></el-option>
              <el-option label="区域二" value="beijing"></el-option>
            </el-select>
            <el-input
              placeholder="输入金额/数量"
              v-model="ruleForm.num2"
              :disabled="true"
              style="width: 300px; margin-left: 15px"
            >
            </el-input> </el-form-item
        ></el-col>
        <el-col :span="12">
          <el-form-item class="line" label="购进指标：" prop="index">
            <el-select
              v-model="ruleForm.index"
              placeholder="金额"
              style="width: 100px"
            >
              <el-option label="区域一" value="shanghai"></el-option>
              <el-option label="区域二" value="beijing"></el-option>
            </el-select>
            <el-input
              placeholder="输入金额/数量"
              v-model="ruleForm.num1"
              :disabled="true"
              style="width: 300px; margin-left: 15px" 
            >
            </el-input> </el-form-item
        ></el-col>
      </el-row>
      <el-row>
        <el-col :span="12">
          <el-form-item label="销售区域：" prop="index">
            <el-button size="small" style="width: 100px">选择区域</el-button>
            <div class="blue el-icon-close">全国</div>
          </el-form-item></el-col
        >
        <el-col :span="12">
          <el-form-item label="签订时间：" prop="time">
            <div class="time">2020-02-01 18:25</div>
          </el-form-item></el-col
        >
      </el-row>
      <el-form-item label="购进渠道：" prop="way" class="modify">
        <div class="">
          <el-select
            style="width: 100px; height: 35px"
            placeholder="指定渠道"
            v-model="ruleForm.way"
          >
            <el-option label="1" value="shanghai"></el-option>
            <el-option label="2" value="beijing"></el-option>
          </el-select>
          <el-button size="small" style="width: 100px; margin-left: 15px"
            >请选择渠道</el-button
          >
        </div>
        <div class="item_table">
          <div class="table_header">
            <div class="header_id">指定渠道编码</div>
            <div class="header_name">指定渠道名称</div>
            <div class="header_address">所在省</div>
          </div>
          <div class="table_body">
            <div class="body_row">
              <div class="row_id">指定渠道编码</div>
              <div class="row_name">指定渠道名称</div>
              <div class="row_address">所在省</div>
            </div>
            <div class="body_row">
              <div class="row_id">指定渠道编码</div>
              <div class="row_name">指定渠道名称</div>
              <div class="row_address">所在省</div>
            </div>
            <div class="body_row">
              <div class="row_id">指定渠道编码</div>
              <div class="row_name">指定渠道名称</div>
              <div class="row_address">所在省</div>
            </div>
          </div>
        </div>
      </el-form-item>
    </el-form>
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
    return {
      ruleForm: {
        name: "",
        status: "",
        time: "",
        way: "",
        num1:"",
        num2:""
      },
      rules: {
        name: [
          { required: true, message: "请选择客户", trigger: "blur" },
          {
            min: 3,
            max: 15,
            message: "长度在 3 到 15 个字符",
            trigger: "blur",
          },
        ],
      },
    };
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
<style lang="less" >
.el-form.top_form{
  background-color: #fff;
    margin-top: 20px;
    /* margin: 15px 25px 0 25px; */
    padding: 15px 25px 0 25px;
  .el-form-item {
    // line-height: 50px;
    margin-bottom: 0px;
    .el-input {
   
    }
    .item_table {
      margin: 10px 0;
      //   padding: 0 30px;
      //   box-sizing: border-box;
      .table_header {
        // margin-top: 10px;
        display: grid;
        grid-template-columns: 1.5fr 2fr 1fr;
        height: 30px;
        line-height: 30px;
        padding: 0 30px;
        background-color: #f8f8f8;
      }
      .table_body {
        // padding: 0 30px;
        .body_row {
          display: grid;
          padding: 0 30px;
          grid-template-columns: 1.5fr 2fr 1fr;
          height: 30px;
          line-height: 30px;
          background-color: #fff;
          border-bottom: 1px solid #e5e5e5;
        }
      }
    }
  }
  .el-form-item {
    .blue {
      vertical-align: middle;
      border: 1px solid #5590fd;
      padding: 10px;
      width: 70px;
      height: 10px;
      margin-left: 15px;
      color: #5590fd;
      border-radius: 5px;
      position: relative;
    }
    .el-icon-close::before {
      position: absolute;
      right: 5px;
      top: 8px;
    }
  }
  .el-form-item.modify {
    .el-select {
      .el-input__inner {
        height: 32px !important;
      }
    }
  }
  .el-form-item {
    vertical-align: middle;
    .time {
      width: 350px;
      height: 31px;
      border: 1px solid #dde0e7;
      padding-left: 10px;
      line-height: 35px;
 
    }
  }
}
</style>

<style lang="less">
.top_form {
  .el-form-item.line {
    .el-form-item__content {
      display: flex;
      .el-select{
        .el-input__inner {
          height: 32px;
        }
      }
      .el-input{
        .el-input__inner{
          height: 32px;
        }
      }
    }
  }
}
</style>