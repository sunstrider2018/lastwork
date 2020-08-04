<template>
  <div>
    <div class="loginUser">
      <div>
        <input type="text" placeholder="请输入手机号/邮箱/用户名" v-model="phonex" />
      </div>
      <div>
        <input type="password" placeholder="输入密码" v-model="psdx" />
        <span class="forgetPsd">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;忘记密码?</span>
      </div>

      <div>
        <input type="text" placeholder="输入图形验证码" />
        <img src />
      </div>
    </div>

    <!-- 登录按钮 -->
    <button @click="handleLoginx">登录</button>

    <!-- 登录方式 -->
    <div class="methods">
      <span>
        <router-link tag="span" to="./LoginP">手机号登录</router-link>
      </span>&nbsp;&nbsp;&nbsp;
      <span>微信登录</span>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "Login",
  data: function () {
    return {
        phonex: this.phonex,
        psdx: this.psdx
    };
  },
  methods: {
   handleLoginx() {
      //点击发送
      let data = new URLSearchParams();
      data.append("phone", this.phone);
      data.append("setpwd", this.psd);
      axios({
        url: "http://10.36.172.30:5050/main/clo/",
        method: "post",
        data: data,
      }).then((res) => {
          if (res.data.code == 1) {
            this.$router.push("/My");
          }else {
            alert("请检查用户名和密码");
          }
        });
    },
  },
};
</script>

<style scoped>
.loginUser {
  width: 5.89rem;
  height: 3.09rem;
  margin-bottom: 0.44rem;
}

.loginUser div {
  width: 100%;
  height: 1.03rem;
  line-height: 1.03rem;
  margin: 0 auto;
  border-bottom: 1px solid #d3d3d3;
}

.loginUser div input {
  font-size: 16px;
  height: 0.8rem;
  border: none;
  padding-top: 0.2rem;
  line-height: 0.8rem;
}

.forgetPsd {
  color: red;
  font-size: 14px;
}

button {
  width: 100%;
  height: 1.05rem;
  border: none;
  background-color: rgb(138, 129, 123);
  font-size: 24px;
  color: cornsilk;
}
.methods {
  width: 100%;
  height: 0.8rem;
  padding-top: 0.3rem;
  color: red;
}
.methods span {
  font-size: 14px;
}
</style>