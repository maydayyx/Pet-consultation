<script setup>
const list = [
    {
        id:1,
        name: '美容',
        imgUrl:'../../../static/icon/美容.png'
    },
    {
        id:2,
        name: '洗澡',
        imgUrl:'../../../static/icon/洗澡.png'
    },
    {
        id:3,
        name: '洁牙',
        imgUrl:'../../../static/icon/洁牙.png'
    },
    {
        id:4,
        name: '剪毛',
        imgUrl:'../../../static/icon/剪毛.png'
    },
    {
        id:5,
        name: '诊疗',
        imgUrl:'../../../static/icon/诊疗.png'
    },
    {
        id:6,
        name: '驱虫',
        imgUrl:'../../../static/icon/驱虫.png'
    },
    {
        id:7,
        name: '疫苗',
        imgUrl:'../../../static/icon/疫苗.png'
    },
    {
        id:8,
        name: '体检',
        imgUrl:'../../../static/icon/体检.png'
    },
]
</script>

<template>
    <view class="category">
    <navigator
      class="category-item"
      hover-class="none"
      url="/pages/index/index"
      v-for="(item, index) in list" :key="item.id"
    >
      <image class="icon" :src="item.imgUrl"></image>
      <text class="text">{{ item.name }}</text>
    </navigator>
  </view>
</template>



<style lang="scss">
.category { 
  margin: 10rpx 0 0;
  padding: 10rpx 0;
  display: flex;
  flex-wrap: wrap;
  min-height: 328rpx;

  .category-item {
    width: 180rpx;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    box-sizing: border-box;
    margin-left: 5rpx;
    .icon {
      width: 100rpx;
      height: 100rpx;
    }
    .text {
      font-size: 26rpx;
      color: #666;
    }
  }
}
</style>