<template>
  <view>
    <nut-popup :style="{}" v-model:visible="showBasic" closeable round>
      <image style="height: 400px" :src="five" :onTap="handleClick" />
      <view class="a" :onTap="handleClick">
        <text class="font-24">个人信用查询</text>
        <text>截止2023年4月</text>
        <text>3000万失信黑名单全网曝光</text>
      </view>
    </nut-popup>
  </view>
</template>
<script setup>
  import { ref } from 'vue';
  import five from '../../../images/five.png';

  const showBasic = ref(true);

  const handleClick = () => {
    console.log(11111222);
  };
</script>
<style>
  .a {
    position: absolute;
    top: 0;
    color: white;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 2.3rem;
    line-height: 0.6rem;
  }
  .nut-popup__close-icon {
    color: white !important;
  }
</style>
