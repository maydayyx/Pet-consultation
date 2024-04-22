<template>
  <!-- 头部 -->
  <view class="nav">
    <image src="../../static/icon/arrow-left.png" alt="" />
    <view class="search">
      <text class="placeholder">请输入您要搜索的商品</text>
      <image src="../../static/icon/search.png" mode="scaleToFill" />
    </view>
    <image
      class="message_icon"
      src="../../../static/icon/购物车.png"
      alt=""
    ></image>
  </view>
  <!-- 沿着y轴滚动的盒子 -->
  <scroll-view scroll-y>
    <!-- 轮播图 -->
    <GuluSwiper :list="list" />
    <!-- 分类 -->
    <view class="category">
      <navigator
        class="category-item"
        hover-class="none"
        url="/pages/index/index"
        v-for="(category, index) in categorylist"
        :key="category.id"
      >
        <image class="icon" :src="category.imgUrl"></image>
        <text class="text">{{ category.name }}</text>
      </navigator>
    </view>
    <!-- 限时秒杀 -->
    <view class="seckill">
      <!-- 标题 -->
      <view class="title">
        <text class="sec">限时秒杀</text>
        <view class="more">
          <text>更多秒杀</text>
          <image src="../../static/icon/arrowRight.png" mode="scaleToFill" />
        </view>
      </view>
      <!-- 商品列表 -->
      <navigator
        class="goods-list"
        url="/pages/index"
        open-type="navigate"
        hover-class="navigator-hover"
        v-for="(goods, index) in seckillList"
        :key="index"
      >
        <!-- 商品图片 -->
        <image :src="goods.imgUrl" mode="scaleToFill" />
        <view class="goods-detail">
          <!-- 商品名称 -->
          <text class="goods-name"
            >{{ goods.goodsName  }}</text
          >
          <view class="time">剩余时间 {{ goods.time }}</view>
          <view class="goods-price">
            <text class="price">￥{{ goods.price }}</text>
            <text class="old-price">￥{{ goods.oldPrice }}</text>
            <text class="sales">月销量{{goods.sales}}+</text>
          </view>
        </view>
      </navigator>
    </view>
  </scroll-view>
</template>

<script setup>
import { time } from 'echarts';

const list = [
  {
    id: 1,
    imgUrl: "../../static/images/商城轮播1.png",
    hrefUrl: "#",
  },
  {
    id: 2,
    imgUrl: "../../static/images/商城轮播2.jpg",
    hrefUrl: "#",
  },
  {
    id: 3,
    imgUrl: "../../static/images/商城轮播3.jpeg",
    hrefUrl: "#",
  },
];
// 分类列表
const categorylist = [
  {
    id: 1,
    name: "主粮",
    imgUrl: "../../static/icon/主粮.png",
  },
  {
    id: 2,
    name: "玩具",
    imgUrl: "../../static/icon/玩具.png",
  },
  {
    id: 3,
    name: "清洁",
    imgUrl: "../../static/icon/清洁.png",
  },
  {
    id: 4,
    name: "用品",
    imgUrl: "../../static/icon/用品.png",
  },
  {
    id: 5,
    name: "分类",
    imgUrl: "../../static/icon/分类.png",
  },
];
// 限时秒杀列表
const seckillList = [
  {
    id:1,
    goodsName:'素力高Solid Gold海洋系列鲭鱼金枪鱼零食罐头 170g',
    time:'01:05:34',
    price:'30.9',
    oldPrice:'59.9',
    sales:'9999',
    imgUrl:'../../static/images/限时秒杀1.jpg'
  },
  {
    id:2,
    goodsName:'路斯 鲣鱼鸡肉虾猫饼干 80g*6 均衡营养猫零食',
    time:'01:05:34',
    price:'19.9',
    oldPrice:'39.9',
    sales:'9999',
    imgUrl:'../../static/images/限时秒杀2.jpg'
  },
  {
    id:3,
    goodsName:'希宝Sheba 吞拿鱼及翡翠虾猫罐头 85g*6罐原装进口',
    time:'01:05:34',
    price:'60.9',
    oldPrice:'99.9',
    sales:'9999',
    imgUrl:'../../static/images/限时秒杀3.jpg'
  },
]
</script>

<style lang="scss">
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20rpx;
  min-height: 100rpx;
  padding: 0 20px;
  image {
    width: 40rpx;
    height: 40rpx;
  }
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
    border: 1px solid #ff9933;
    background-color: #fff;

    .placeholder {
      color: #ccc;
    }
  }
  .message_icon {
    width: 55rpx;
    height: 55rpx;
  }
}

.category {
  display: flex;
  min-height: 100rpx;
  margin: 20px;
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

.seckill {
  display: flex;
  flex-direction: column;
  .title {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 50rpx;
    margin-top: 30rpx;
    .sec {
      font-size: 36rpx;
      font-weight: bold;
    }
    .more {
      display: flex;
      align-items: center;
      text {
        font-size: 30rpx;
        color: #a0a0a0;
        margin-right: 15rpx;
      }
      image {
        width: 35rpx;
        height: 50rpx;
      }
    }
  }
  .goods-list {
    display: flex;
    flex-direction: row;
    margin: 30rpx 50rpx;
    image {
      width: 400rpx;
      height: 200rpx;
      margin-right: 20rpx;
    }
    .goods-detail {
      display: flex;
      flex-direction: column;
      .goods-name {
        overflow: hidden;
      }
      .time {
        font-size: 25rpx;
        margin: 10rpx 0;
        color: #ccc;
      }
      .goods-price {
        display: flex;
        justify-content: space-between;
        align-items: center;
        .price {
          margin-left: 3rpx;
          color: #ff9933;
          font-weight: bold;
          font-size: 35rpx;
        }
        .old-price {
          font-size: 25rpx;
          padding: 10rpx 25rpx 0 0rpx;
          text-decoration: line-through;
          color: #ccc;
        }
        .sales {
          font-size: 20rpx;
          color: #bbb;
        }
      }
    }
  }
}
</style>
