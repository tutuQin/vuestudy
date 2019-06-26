<template>
  <div class="login_test">
    <div class="title-container">
      <h3 class="title">
        User Login
      </h3>
    </div>
    <div class="formbox">
      <el-form
        ref="form"
        :model="form"
      >
        <el-form-item>
          <span class="svg-container">
            <svg-icon icon-class="user" />
          </span>
          <el-input 
            v-model="form.name" 
            placeholder="请输入账号"
            name="username"
          />
        </el-form-item>
        <el-tooltip
          v-model="capsTooltip"
          content="Caps lock is On"
          placement="right"
          manual
        >
          <el-form-item prop="password">
            <span class="svg-container">
              <svg-icon icon-class="password" />
            </span>
            <el-input 
              v-model="form.password" 
              placeholder="请输入密码" 
              show-password
            />
          </el-form-item>
        </el-tooltip>
        <el-row>
          <el-button 
            type="primary"
            style="width:100% ; padding:16px 0;"
            @click="dayin()"
          >
            确定
          </el-button>
        </el-row>
      </el-form>
      <div>
        <p
          class="zhxx"
          style="color:#fff;float:left"
        >
          账号：abcd     密码：12345
          <br>
          账号：abcd     密码：12345
        </p>
        <span
          class="qqwechat"
          style="float:right;padding-top:16px;"
        >
          <el-row>
            <el-button 
              type="success"
              style="width:160px ; padding:12px 0;"
              @click="1"
            >
              其他账户登陆
            </el-button>
          </el-row>
        </span>      
      </div>
      <br>
      <!-- <div style="max-width:500px ;width:80%; padding:14px 0;color:#fff;font-size:16px;padding-top:12px;" >{{form.name}}{{form.password}} </div> -->
    </div>
  </div>
</template>

<script>

export default {
  name: 'LoginTest',

  components: {},
  data() {
    return {
      form:{
      name:'',
      password:''
      },
      capsTooltip: true,
    }
  },

  computed: {
  },

  watch: {},

  beforeMount(){},

  mounted(){},
  

  methods: {
    dayin(){
   } 
  }
}

</script>
/* 全局css */
<style lang='scss'>
    .el-input{
       width:80%;
      line-height: 60px;
       display: inline-block;
      
       input{
          background: #283442;
          border: 0px;
          -webkit-appearance: none;
          border-radius: 0px;
          // padding: 24px 0px 12px 15px;
          color: #ffffff;
          line-height: 60px;
          caret-color: #899aa3;
        }

    }
     .el-form-item {
      border: 1px solid rgba(255, 255, 255, 0.1);
      background: rgba(0, 0, 0, 0.1);
      border-radius: 5px;
      color: #899aa3;
      }
   .svg-container {
    // padding: 6px 5px 6px 15px;
    padding-left: 16px;
 
    vertical-align: middle;
    width:15%;
    display: inline-block;
  }
</style>




<style lang='scss' scoped>
   

    .login_test{
      height: 100vh;
      width: 100%;
      background-color: #2d3a4b;
      overflow: hidden;

    }
    .formbox{
          width: 80%;
          max-width: 480px;
          margin: 0 auto;


        }
  .title-container {
      margin-top: 140px;

    .title {
      font-size:28px;
      color:#fff;
      margin: 40px auto 40px auto;
      text-align: center;
    }
 
    .show{
      font-size: 16px;
      color: #fff;
    
    }
   @media only screen and (max-width: 470px) {
    .qqwechat {
      display: none;
    }
  }

  }

</style>