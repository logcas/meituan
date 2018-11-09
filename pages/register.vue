<template>
    <div class="register">
        <div class="header">
            <div class="center-container">
                <a href="/" class="logo"></a>
                <div class="login-block">
                    <span>已有美团账号？</span>
                    <nuxt-link class="login-btn" to="/login">登录</nuxt-link>
                </div>
            </div>
        </div>
        <div class="content">
            <el-form
                :model="ruleForm2"
                status-icon
                :rules="rules2"
                ref="ruleForm2"
                label-width="100px"
                class="demo-ruleForm"
            >
                <el-form-item label="电子邮箱" prop="email">
                    <el-input v-model="ruleForm2.email" style="width:248px"></el-input>
                </el-form-item>
                <el-form-item label="动态验证码" prop="validateCode">
                    <el-input v-model="ruleForm2.validateCode" autocomplete="off" style="width:248px"></el-input>
                </el-form-item>
                <el-form-item label="密码" prop="pass">
                    <el-input
                        type="password"
                        v-model="ruleForm2.pass"
                        autocomplete="off"
                        style="width:248px"
                    ></el-input>
                </el-form-item>
                <el-form-item label="确认密码" prop="checkPass">
                    <el-input
                        type="password"
                        v-model="ruleForm2.checkPass"
                        autocomplete="off"
                        style="width:248px"
                    ></el-input>
                </el-form-item>
                <el-form-item>
                    <el-button type="primary" @click="submitForm('ruleForm2')" class="btn">同意以下协议并注册</el-button>
                </el-form-item>
                <el-form-item>
                    <a class="f1" href="http://www.meituan.com/about/terms" target="_blank">《美团网用户协议》</a>
                </el-form-item>
            </el-form>
        </div>
    </div>
</template>

<script>
export default {
  layout: "empty",
  data() {
    var checkEmail = (rule, value, callback) => {
      if (!value) {
        return callback(new Error("电子邮箱不能为空"));
      }
      setTimeout(() => {
        if (!/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/.test(value)) {
          callback(new Error("请输入正确的电子邮箱地址"));
        } else {
            callback();
        }
      }, 1000);
    };
    var checkValidateCode = (rule, value, callback) => {
        if(!value) {
            return callback(new Error("请输入动态验证码"));
        } else {
            callback();
        }
    }
    var validatePass = (rule, value, callback) => {
      if (value === "") {
        callback(new Error("请输入密码"));
      } else {
        if (this.ruleForm2.checkPass !== "") {
          this.$refs.ruleForm2.validateField("checkPass");
        }
        callback();
      }
    };
    var validatePass2 = (rule, value, callback) => {
      if (value === "") {
        callback(new Error("请再次输入密码"));
      } else if (value !== this.ruleForm2.pass) {
        callback(new Error("两次输入密码不一致!"));
      } else {
        callback();
      }
    };
    return {
      ruleForm2: {
        pass: "",
        checkPass: "",
        email: "",
        validateCode: "",
      },
      rules2: {
        pass: [{ validator: validatePass, trigger: "blur" }],
        checkPass: [{ validator: validatePass2, trigger: "blur" }],
        email: [{ validator: checkEmail, trigger: "blur" }],
        validateCode: [{ validator: checkValidateCode, trigger: "blur"}]
      }
    };
  },
  methods: {
    submitForm(formName) {
      this.$refs[formName].validate(valid => {
        if (valid) {
          alert("submit!");
        } else {
          console.log("error submit!!");
          return false;
        }
      });
    },
  }
};
</script>

<style lang="scss" scoped>
.register {
  font: 400 14px/1.5 "Hiragino Sans GB", "WenQuanYi Micro Hei", tahoma,
    sans-serif;
  color: #666;
}

.center-container {
  margin: 0 auto;
  padding: 10px 0;
  width: 980px;
}

.header {
  border-bottom: 2px solid #2bb8aa;
  min-width: 980px;
  color: #666;

  .logo {
    display: inline-block;
    width: 54px;
    height: 36px;
    background-position: -669px -748px;
    background-image: url(https://s0.meituan.net/bs/file/?f=fe-sso-fs:build/assets/sp-normal.2ee5c09.png);
  }

  .login-block {
    float: right;
    line-height: 36px;

    span {
      margin-right: 10px;
      vertical-align: sub;
    }

    .login-btn {
      color: #fff;
      padding: 6px 10px;
      font-size: 12px;
      background: #2db3a6;
      background-image: linear-gradient(to bottom, #2ec3b4, #2db3a6);
    }
  }
}

.content {
  margin: 0 auto 30px;
  padding-top: 30px;
  width: 980px;
  min-height: 300px;
}

.btn {
    background-color: #2db3a6;
    background-image: linear-gradient(to bottom,#2ec3b4,#2db3a6);
}

.f1 {
    display: inline-block;
    padding-top: -20px;
    color: #2db3a6;
}
</style>
