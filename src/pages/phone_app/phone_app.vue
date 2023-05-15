<template>
  <view class="top-text">以下手机银行APP可查询信用</view>
  <view>
    <image style="width: 100%; height: 700px" :src="phone1" />
  </view>
  <view>
    <image style="width: 100%; height: 700px" :src="phone2" />
  </view>
  <view>
    <image style="width: 100%; height: 700px" :src="phone3" />
  </view>
  <view class="text-grey text-center mt-20">*页面信息仅供参考</view>
  <nut-button block class="my-button" type="info" :onTap="backIndex">返回首页</nut-button>
</template>

<script setup>
  import phone1 from '../../../images/phone1.png';
  import phone2 from '../../../images/phone2.png';
  import phone3 from '../../../images/phone3.png';
</script>

<style>
  .top-text {
    margin-left: 30px;
    margin-bottom: 20px;
  }
</style>
