<script setup lang="ts">
//获取屏幕边界到安全区域距离
const { safeAreaInsets } = uni.getSystemInfoSync();
</script>

<template>
  <view class="navbar" :style="{ paddingTop: safeAreaInsets?.top + 'px' }">
    <view class="search">
        <text class="placeholder">请输入搜索内容</text>
    </view>
    <image class="message_icon" src="../../../static/icon/信息.png" alt=""></image>
  </view>
</template>

<style lang="scss">
/* 自定义导航条 */
.navbar {
  display: flex;
  justify-content: space-evenly;
  align-items:center;
  height: 100px;
  background-color: #fff;
  padding-left: 30rpx;
  padding-top: 20rpx;

  .search {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 10rpx 0 26rpx;
    width: 70%;
    height: 64rpx;
    margin: 16rpx 20rpx;
    color: #fff;
    font-size: 28rpx;
    border-radius: 32rpx;
    border: 1px solid #FF9933;
    background-color: #fff;

    .placeholder {
      color: #ccc;
    }
  }
  .message_icon {
    width: 60rpx;
    height: 60rpx;
  }
}
</style>
