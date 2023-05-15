<template>
  <view class="aaa">
    <text class="font-24">个人信用官网地址</text>
    <text>https://ipcrs.pbccrc.org.cn/</text>
  </view>
  <view>
    <image style="width: 100%; height: 500px" :src="person" />
  </view>
  <view class="text-grey mt-20 text-center">
    <text>
      *网上查询渠道只能查询您本人的电子版信用报告，请您注意，切勿将信用报告提供给他人或其他机构。
    </text>
  </view>
  <view class="text-grey mt-20 flex justify-center">*页面信息仅供参考</view>
  <nut-button block class="my-button" type="info" :onTap="backIndex">返回首页</nut-button>
</template>

<script setup>
  import person from '../../../images/person1.png';
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
