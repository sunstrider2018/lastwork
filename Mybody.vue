<template>
  <div class="Mysort">
    <div class="icon1">
      <div class="inP1">
        <span class="iconfont icon-dingdan-"></span>
      </div>
      <p>我的订单</p>
    </div>
    <div class="icon2">
      <div class="inP2">
        <span class="iconfont icon-dunpai"></span>
      </div>
      <p>我的保险</p>
    </div>
    <div class="icon3">
      <div class="inP3">
        <span class="iconfont icon-yixianshi-"></span>
      </div>
      <p>我的理赔</p>
    </div>
    <div class="icon4">
      <div class="inP4">
        <span class="iconfont icon-qiandai"></span>
      </div>
      <p>我的资产</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Mybody",
  data: function () {
    return {};
  },
};
</script>


<style scoped>
.Mysort {
  height: 2.14rem;
  width: 100%;
  margin: 0 auto;
  background: #fff;
  display: flex;
  justify-content: space-around;
}
.icon1,
.icon2,
.icon3,
.icon4 {
  width: 1.4rem;
  height: 1.4rem;
  background: #fff;
  margin: 0.2rem auto;
  text-align: center;
}
span {
  color: white !important;
  font-size: 0.65rem !important ;
}
p {
  margin-top: 15px;
}
.inP1 {
  width: 0.78rem;
  height: 0.78rem;
  background-color: yellow;
  text-align: center;
  line-height: 40px;
  margin-left: 16px;
  border-radius: 10px;
  box-shadow: 0 3px rgb(245, 240, 168);
}
.inP2 {
  width: 0.78rem;
  height: 0.78rem;
  background-color: purple;
  text-align: center;
  line-height: 40px;
  margin-left: 16px;
  border-radius: 10px;
  box-shadow: 0 3px rgb(224, 172, 226);
}
.inP3 {
  width: 0.78rem;
  height: 0.78rem;
  background-color: orangered;
  text-align: center;
  line-height: 40px;
  margin-left: 16px;
  border-radius: 10px;
  box-shadow: 0 3px rgb(223, 182, 159);
}
.inP4 {
  width: 0.78rem;
  height: 0.78rem;
  background-color: blue;
  text-align: center;
  line-height: 40px;
  margin-left: 16px;
  border-radius: 10px;
  box-shadow: 0 3px rgb(175, 189, 235);
}
</style>