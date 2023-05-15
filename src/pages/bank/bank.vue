<template>
  <view class="aaa">
    <text class="font-24">以下银行网银可查询信用</text>
    <text>通过网银查询信用需在电脑端登录</text>
  </view>
  <view>
    <image style="width: 100%; height: 500px" :src="bank" />
  </view>
  <view class="text-grey text-center mt-20">*页面信息仅供参考</view>
  <nut-button block class="my-button" type="info" :onTap="backIndex">返回首页</nut-button>
</template>

<script setup>
  import bank from '../../../images/bank1.png';
  import Taro from '@tarojs/taro';

  const backIndex = () => {
    Taro.redirectTo({
      url: '/pages/index/index',
    });
  };
</script>

<style>
  .aaa {
    height: 1.6rem;
    background: white;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding-left: 20px;
    border-radius: 10px;
    margin-bottom: 20px;
  }
</style>
