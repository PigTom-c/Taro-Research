<template>
  <view class="w-100" v-if="!isLink">
    <button type="primary" class="w-200" plain :onTap="handleClick">请点击查询</button>
<!--    <text>借了东西为什么不还</text>
    <text>你的背包 让我走得好缓慢</text>-->
  </view>
  <web-view v-else src='https://www.baidu.com' />
</template>

<script lang="ts" setup>
import { ref } from 'vue'

    const isLink = ref(false)

    const handleClick = () => {
      isLink.value = !isLink.value
      console.log('click')
      my.ap.openURL

    }


</script>

<style>
 .w-100 {
   display: flex;
   justify-content: center;
   flex-direction: column;
   line-height: 50px;
 }
 .w-200 {
   width: 200px;
 }
</style>
