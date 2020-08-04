<template>
  <div>
    <div class="bottom">
      <div class="bottom-t">注册即代表您已阅读并同意</div>
      <div class="bottom-b">中国人民保险集团股份有限公司服务协议</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Loginb",
  data: function () {
    return {};
  },
};
</script>

<style scoped>
.bottom {
  position: fixed;
  bottom: 0;
  width: 80%;
  height: 1.44rem;
}
.bottom-t {
  font-size: 16px;
  text-align: center;
  padding-top: 0.22rem;
  margin-bottom: 0.1rem;
}
.bottom-b {
  font-size: 16px;
  color: #3982de;
  padding-bottom: 0.22rem;
}
</style>