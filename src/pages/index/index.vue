<template>
  <view>
    <image style="width: 100%; height: 100px" :src="namePng" :onTap="handleClick" />
  </view>

  <view>
    <List />
  </view>
  <view class="mt-20" :onTap="handleClick">
    <image style="width: 100%; height: 110px" :src="four" />
  </view>
  <Modal />
</template>

<script lang="ts" setup>
  import { ref, onMounted } from 'vue';
  import './index.less';
  import namePng from '../../../images/bg_top.png';
  import four from '../../../images/four.png';
  import List from '../../components/list/index';
  import Taro from '@tarojs/taro';
  import Modal from '../../components/modal/index';

  onMounted(() => {});

  const handleClick = () => {
    //
  };
</script>

<style></style>
