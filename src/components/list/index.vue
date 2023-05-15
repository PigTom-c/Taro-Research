<template>
  <view class="bg-center">
    <view class="font-24 ml-10">个人信用官方查询渠道</view>
    <view class="font-16 ml-10">
      包含以下3种查询渠道
      <Icon size="60" type="warn" color="red" />
    </view>
    <view :onTap="handleTop">
      <image style="width: 100%; height: 100px" :src="one" />
    </view>
    <view :onTap="handleCenter">
      <image style="width: 100%; height: 100px" :src="two" />
    </view>
    <view :onTap="handleBottom">
      <image style="width: 100%; height: 100px" :src="three" />
    </view>
  </view>

  <!--  <web-view v-else src='https://www.chayouxin.com/query/#/Home3?cid=393&templateId=3' />-->
</template>

<script setup lang="ts">
  import one from '../../../images/one.png';
  import two from '../../../images/two.png';
  import three from '../../../images/three.png';
  import Taro from '@tarojs/taro';

  const handleTop = () => {
    Taro.navigateTo({ url: '/pages/thread_detail/thread_detail' });
  };

  const handleCenter = () => {
    Taro.showModal({
      title: '银行柜台查询',
      content:
        '本人可持有效身份证件原件到中国人民银行市级分行营业管理部信用服务大厅及所辖支行信用查询柜台办理，每年有2次免费查询机会，超过次数每次收取10元服务费',
      showCancel: false,
      success: function (res) {
        if (res.confirm) {
          console.log('用户点击确定');
        } else if (res.cancel) {
          console.log('用户点击取消');
        }
      },
    });
  };

  const handleBottom = () => {
    Taro.showModal({
      title: '自助机查询',
      content:
        '信用报告查询服务网点自助机，每年同样可免费查询2次机会。超过2次的，需要到信用查询柜台申请查询，并收取服务费10元/次。',
      showCancel: false,
    });
  };
</script>

<style lang="less">
  .bg-center {
    height: 9rem;
    line-height: 1rem;
    background: white;
    display: flex;
    justify-content: center;
    padding: 0 20px;
    flex-direction: column;
    border-radius: 16px;
    margin-top: 20px;
  }
</style>
