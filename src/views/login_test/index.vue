<template>
  <div class="login_test">
    <el-form ref="loginForm" :model="loginForm" :rules="loginRules" class="login_test-form" autocomplete="on" label-position="left">
      <div class="title-container">
        <h3 class="title">登陆</h3>
      </div>
      <el-form-item prop="username">
        <span class="svg-container">
          <svg-icon icon-class="user" />
        </span>
        <el-input
          ref="username"
          v-model="loginForm.username"
          placeholder="Username"
          name="username"
          type="text"
          tabindex="1"
          autocomplete="on"
        />
      </el-form-item>
    </el-form>
  </div>
</template>

<script>

export default {
  name: 'LoginTest',

  components: {},
  props: [''],
  data() {
    return {

    }
  },

  computed: {},

  watch: {},

  beforeMount() {},

  mounted() {},

  methods: {}

}

</script>
<style lang='scss' scoped>
    $bg:#2d3a4b;
    $light_gray:#fff;
    $cursor: #fff;
    .login_test{
      min-height: 100%;
      width: 100%;
      background-color: #2d3a4b;
      overflow: hidden;

       .login_test-form {
          position: relative;
          width: 520px;
          max-width: 100%;
          padding: 160px 35px 0;
          margin: 0 auto;
          overflow: hidden;
        }
    }

  .title-container {
    position: relative;

    .title {
      font-size: 26px;
      color: $light_gray;
      margin: 0px auto 40px auto;
      text-align: center;
      font-weight: bold;
    }
  }

</style>
