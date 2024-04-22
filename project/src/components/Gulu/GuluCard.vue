<script setup>
</script>

<!-- 
  这是一个组件，封住了一个卡片，通过插槽传递不同的样式和数据，方便复用
 -->

<template>
  <!-- 一张卡片 -->
  <view class="card">  
    <!-- 遮罩层--背景颜色 -->
    <view class="shadow">
      <!-- 通过插槽在使用的地方传来一个背景遮罩 -->
      <slot name="shadow"></slot>
    </view>
    <!-- 背景图 -->
    <view class="bg">
     <slot name="bg">

     </slot>
    </view>
    <view class="title">
      <slot name="title"> </slot>
    </view>
    <view class="footer">
      <slot name="footer"> </slot>
    </view>
  </view>
</template>

<style lang="scss">
.card {
  position: relative;
  margin: 0 10rpx;
  width: 220rpx;
  height: 250rpx;
  text-align: center;
  border-radius: 10%;
  .bg {
    position: absolute;
    top: 0;
    left: 0;
    box-shadow: 0 0 10rpx #ccc;
    border-radius: 10%;
    image {
      width: 220rpx;
      height: 240rpx;
      border-radius: 10%;
    }
  }
  .title {
    z-index: 9999;
    position: absolute;
    top: 110rpx;
    left: 45%;
    transform: translate(-50%, -50%);
    text-align: center;
    text {
      hyphens: auto;
      font-size: 30rpx;
      color: #fff;
      font-weight: bold;
    }
  }
  .footer {
    text-align: center;
    z-index: 9999;
    position: absolute;
    top: 200rpx;
    left: 35rpx;
    text {
      font: 20rpx;
      color: #fff;
    }
  }
}
</style>
