<script setup></script>

<template>
  <view class="container">
    <view class="left">
      <image src="../../../static/icon/预约挂号.png" mode="scaleToFill" />
      <text>预约挂号</text>
    </view>
    <view class="right">
      <view class="top">
        <image src="../../../static/icon/健康检测.png" mode="scaleToFill" />
        <text>健康检测</text>
      </view>
      <view class="bottom">
        <image src="../../../static/icon/专家问诊.png" mode="scaleToFill" />
        <text>专家问诊</text>
      </view>
    </view>
    <view class="footer">
      <image src="../../../static/icon/宠物档案.png" mode="scaleToFill" />
      <text>宠物档案</text>
    </view>
  </view>
</template>

<style lang="scss">
.container {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  flex-direction: row;
  margin: 25rpx;
  background-color: #fff;
  min-height: 500rpx;
  padding: 20rpx;
  .left {
    flex: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
    width: 280rpx;
    height: 500rpx;
    box-shadow: 0 0 10rpx #ccc;
    image {
      width: 280rpx;
      height: 300rpx;
    }
    text {
      text-align: center;
      padding-top: 60rpx;
      color: #000;
      font-size: 50rpx;
      letter-spacing: 0.2em;
      font-weight: bold;
      color: #c0c0c0;
    }
  }
  .right {
    margin-left: 20rpx;
    flex: 2;
    display: flex;
    flex-direction: column;
    height: 500rpx;
    box-shadow: 0 0 10rpx #ccc;
    .top {
      flex: 1;
      display: flex;
      align-items: center;
      height: 250rpx;
      image {
        width: 180rpx;
        height: 200rpx;
      }
      text {
        padding: 0 10rpx;
        letter-spacing: 0.1em;
        font-size: 30rpx;
        font-weight: bold;
        color: #c0c0c0;
      }
    }
    .bottom {
      flex: 1;
      display: flex;
      align-items: center;
      height: 250rpx;
      border-top: 1px solid #ddd7d7;
      image {
        width: 180rpx;
        height: 200rpx;
      }
      text {
        padding: 0 10rpx;
        letter-spacing: 0.1em;
        font-size: 30rpx;
        font-weight: bold;
        color: #c0c0c0;
      }
    }
  }
  .footer {
    display: flex;
    flex: 1;
    justify-content: space-evenly;
    align-items: center;
    height: 250rpx;
    padding: 0 50rpx;
    margin-top: 30rpx;
    box-shadow: 0 0 10rpx #ccc;
    image {
      flex: 2;
      width: 100px;
      height: 100px;
    }
    text {
      flex: 3;
      font-size: 50rpx;
      font-weight: bold;
      color: #c0c0c0;
      letter-spacing: 0.3em;
      margin-left: 20rpx;
    }
  }
}
</style>
