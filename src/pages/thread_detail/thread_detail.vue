<template>
  <view class="main">
    <view>
      <text class="font-24">
        请选择网上查询渠道 \n
        <text class="font-16">个人信用网上查询包含以下3种查询渠道</text>
      </text>
    </view>
    <view class="main-item font-24 mt-20" :onTap="person">人行信用中心官网</view>
    <view class="main-item font-24 mt-30" :onTap="bank">银行网银</view>
    <view class="main-item font-24 mt-30" :onTap="phoneApp">手机银行app</view>
  </view>
  <view class="mt-30">
    <text class="text-grey font-18">
      *网上查询渠道只能查询您本人的电子版信用报告，请您注意，切勿将信用报告提供给他人或其他机构。
    </text>
  </view>
  <nut-button block class="my-button" type="info" :onTap="backIndex">返回首页</nut-button>
</template>
<script setup>
  import Taro from '@tarojs/taro';

  const person = () => {
    Taro.navigateTo({ url: '/pages/person/person' });
  };

  const bank = () => {
    Taro.navigateTo({ url: '/pages/bank/bank' });
  };

  const phoneApp = () => {
    Taro.navigateTo({ url: '/pages/phone_app/phone_app' });
  };

  const backIndex = () => {
    Taro.redirectTo({
      url: '/pages/index/index',
    });
  };
</script>
<style>
  .main {
    display: flex;
    /*justify-content: center;*/
    flex-direction: column;
    background: white;
    height: 6.5rem;
    line-height: 1rem;
    padding: 0 20px;
    border-radius: 16px;
  }
  .main-item {
    border-radius: 1.2rem;
    border: 1px solid gray;
    color: #4f4fd1;
    display: flex;
    justify-content: center;
  }
</style>
