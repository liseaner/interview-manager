<!--  -->
<template>
  <div class="text">
    <div class="content">
      <div class="top">
        <el-button type="primary" size="mini" style="font-size:14px">添加产品</el-button>
        <div class="index1">
          购进总指标（万元）：<b>￥152.65</b>
        </div>
        <div class="index1">
          指标嫉妒分节（万元）：<b>[Q1]￥12.5,[Q4]￥12.5</b>
        </div>
        <div class="index1">纯销指标量:<b>￥152.65</b></div>
      </div>
      <div class="product">
        <el-form :model="proForm">
          <el-row>
            <el-col :span="10">
              <el-form-item label="产品：" prop="pro" class="line2">
                <el-button size="medium">选择产品</el-button>&nbsp;&nbsp;
                <span class="blue2">美复胶丸&nbsp;24粒/盒</span>
              </el-form-item>
            </el-col>
            <el-col :span="8">
              <el-form-item label="协议效期：" prop="pro" class="line2">
                <el-button size="medium"
                  >2020-02-01&nbsp;~&nbsp;2020-05-01</el-button
                >&nbsp;&nbsp;
              </el-form-item>
            </el-col>
          </el-row>
        </el-form>
        <div class="delete">删除</div>
      </div>
      <div class="block1">
        <div class="price">
          <div class="price1"><b>协议价(元)</b></div>
          <div class="price1"><b>协议价(元)</b></div>
          <div class="price1"><b>协议价(元)</b></div>
          <div class="price1"><b>协议价(元)</b></div>
          <div class="price1"><b>协议价(元)</b></div>
          <div class="price1"><b>协议价(元)</b></div>
          <div class="price1"><b>协议价(元)</b></div>
          <div class="blank">
            <el-input v-model="proForm.text" placeholder="请输入"></el-input>
          </div>
          <div class="blank">
            <el-input v-model="proForm.text" placeholder="请输入"></el-input>
          </div>
          <div class="blank">
            <el-input v-model="proForm.text" placeholder="请输入"></el-input>
          </div>
          <div class="blank">
            <el-input v-model="proForm.text" placeholder="请输入"></el-input>
          </div>
          <div class="blank">
            <el-input v-model="proForm.text" placeholder="请输入"></el-input>
          </div>
          <div class="blank">
            <el-input v-model="proForm.text" placeholder="请输入"></el-input>
          </div>
          <div class="blank">
            <el-input v-model="proForm.text" placeholder="请输入"></el-input>
          </div>
        </div>
      </div>
      <div class="block2">
        <div class="tasks">
          <div class="task"><b>协议价(元)</b></div>
          <div class="task"><b>协议价(元)</b></div>
          <div class="task"><b>协议价(元)</b></div>
          <div class="task"><b>协议价(元)</b></div>
          <div class="task"><b>协议价(元)</b></div>
          <div class="task"><b>协议价(元)</b></div>
          <div class="task"><b>协议价(元)</b></div>
          <div class="task"><b>协议价(元)</b></div>
          <div class="blank">
            <el-input v-model="proForm.text" placeholder="请输入"></el-input>
          </div>
          <div class="blank">
            <el-select
              style="width: 200px; height: 32px"
              v-model="proForm.course1"
              placeholder="单选项1"
            >
              <el-option label="1" value="shanghai"></el-option>
              <el-option label="2" value="beijing"></el-option>
            </el-select> 
          </div>
          <div class="blank">
            <el-input v-model="proForm.text" placeholder="请输入"></el-input>
          </div>
          <div class="blank">
            <el-select
              style="width: 200px; height: 32px"
              v-model="proForm.course2"
              placeholder="多选项1"
            >
              <el-option label="1" value="shanghai"></el-option>
              <el-option label="2" value="beijing"></el-option>
            </el-select> 
          </div>
          <div class="blank">
            <el-input v-model="proForm.text" placeholder="请输入"></el-input>
          </div>
          <div class="blank">
            <el-select
              style="width: 200px; height: 32px"
              v-model="proForm.course3"
              placeholder="多选项1"
            >
              <el-option label="1" value="shanghai"></el-option>
              <el-option label="2" value="beijing"></el-option>
            </el-select> 
          </div>
          <div class="blank">
            <el-button size="medium"
                  >2020-05-15</el-button
                >&nbsp;&nbsp;
          </div>
          <div class="blank">
            <el-button size="medium"
                  >2020-05-15</el-button
                >&nbsp;&nbsp;
          </div>
        </div>
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
    return {
      proForm: {
        pro: "",
        course1:"",
        course2:"",
        course3:""
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
  <style lang="less">
.text {
  //   background-color: #fff;
  margin-top: 16px;
  font-size:14px;
  //   padding: 10px 0px;
  .content {
    position: relative;
    // display: flex;
    .top {
      width: 100%;
      height:34px;
      display: flex;
      margin-bottom: 10px;
      .el-button {
        font-size: 18px;
        // position: absolute;
        // top: -13px;
        // left: 0px;
        height: 34px;
        display: block;
      }
      .index1 {
        width: auto;
        padding: 0 20px;
        text-align: center;
        line-height: 34px;
        color: #7b7b7b;
      }
      .active {
        color: #2998fe;
        font-weight: 500;
      }
    }
    .product {
      width: 100%;
    height: 35px;
    padding: 10px 0px;
    background-color: #fff;
    position: relative;
    .el-form{
      height: 35px;
      .el-form-item.line2{
        height: 35px;
        margin-bottom:0 ;
        .el-button{
          height: 32px;
          // line-height: ;
        }
      }
    }
      .delete {
        width: 60px;
        height: 25px;
        color: #fea428;
        border: 1px solid #ccc;
        position: absolute;
        top: 17px;
        right: 5px;
        text-align: center;
        line-height: 25px;
        border-radius: 5px;
      }
      //   border: 1px solid #ccc;
      //   display: flex;
      //   align-items: center;
      .el-form {
        margin-left: 20px;
      }
      .el-form-item.line {
        .el-form-item__content {
          display: flex;
          .blue2 {
            color: #2998fe;
            width: 100px;
            height: 40px;
          }
        }
      }
    }
    .block1 {
      box-shadow: #7b7b7b;
      width: calc(100% - 40px);
      border-top: 2px solid #efefef;
      height: 84px;
      position: relative;
      padding: 10px 20px;
      background-color: #fff;
      color: #505050;
      .price {
        border: 1px solid #ededed;
        display: grid;
        grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
        grid-template-rows: 1fr 1.5fr;
        height: 83px;
        .price1 {
          padding: 8px 10px 10px 10px;
          border-bottom: 1px solid #ededed;
          background-color: #f8f8f8;
          font-size: 14px;
          height: 15px;
        }
        .blank {
          .el-input {
          width: 180px;
          padding: 8px 0 0 10px;
          .el-input__inner {
            background-color: #f8f8f8;
            height: 32px;
          }
        }
        }

       
      }
    }
    .block2{
      width: calc(100% - 40px);
      // border-top: 2px solid #efefef;
      height: 100px;
      position: relative;
      padding: 5px 20px;
      background-color: #fff;
      color: #505050;
      .tasks{
        border: 1px solid #ededed;
        display: grid;
        grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
        grid-template-rows: 1fr 1.3fr;
        height: 88px;
        .task{
          padding: 8px 10px 10px 10px;
          border-bottom: 1px solid #ededed;
          background-color: #f8f8f8;
          font-size: 14px;
          height: 15px;
        }
      .blank{
        .el-input {
          width: 180px;
          height: 35px;
       &:first-child{
        padding: 8px 0 0 10px;
       }
          .el-input__inner {
            background-color: #f8f8f8;
            height: 32px;
            
          }
        }
        .el-select{
          width: 180px;
          height: 36px;
          // padding: 10px 0 0 10px;
          padding: 0 10px;
          .el-input__inner{
            // height: 36px;
          }
        }
        .el-button{
          // padding: 10px 0 0 10px;
          margin: 10px 0 0 20px;
          width: 180px;
          &:first-child{
            margin-left: -5px;
          }
        }
      }
        
      }
    }
  }
}
</style>

<style lang="less">
.price {
  .blank {
    .el-input__inner {
      background-color: #e4e2e7;
      color: #a8a1a8;
      &.el-input__inner:focus {
        background-color: #fff;
      }
    }
  }
}
</style>