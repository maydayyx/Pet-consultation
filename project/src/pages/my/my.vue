<script setup></script>

<template>
  <view class="nav">
    <view class="arrow-left">
      <image src="../../static/icon/arrow-left.png" mode="scaleToFill" />
    </view>

    <view class="setting">
      <image src="../../static/icon/设置.png" mode="scaleToFill" />
      <image src="../../static/icon/铃铛.png" mode="scaleToFill" />
    </view>
  </view>
  <view class="info">
    <view class="avatar">
      <image src="../../static/images/宠物图10.jpeg" mode="scaleToFill" />
    </view>
    <view class="intro">
      <text class="name">小七七</text>
      <text class="desc">姐是最棒的.....</text>
    </view>
    <view class="arrow-right">
      <image src="../../static/icon/arrowRight.png" mode="scaleToFill" />
    </view>
  </view>
  <view class="nums">
    <view class="num">
      <text>249</text>
      <text>关注</text>
    </view>
    <view class="num">
      <text>1249</text>
      <text>粉丝</text>
    </view>
    <view class="num">
      <text>2459</text>
      <text>获赞</text>
    </view>
  </view>
  <!-- 我的订单 -->
  <view class="my-order">
    <!-- 标题 -->
    <view class="title">
      <text class="topic">我的订单</text>
      <view class="more">
        <text>查看全部</text>
        <image src="../../static/icon/arrowRight.png" mode="scaleToFill" />
      </view>
    </view>
    <view class="order-btn-list">
      <navigator
        class="order-btn"
        url="/pages/"
        open-type="navigate"
        hover-class="navigator-hover"
      >
        <image src="../../static/icon/待付款.png" mode="scaleToFill" />
        <text class="order-name">待付款</text>
      </navigator>
      <navigator
        class="order-btn"
        url="/pages/"
        open-type="navigate"
        hover-class="navigator-hover"
      >
        <image src="../../static/icon/待收货.png" mode="scaleToFill" />
        <text class="order-name">待收货</text>
      </navigator>
      <navigator
        class="order-btn"
        url="/pages/"
        open-type="navigate"
        hover-class="navigator-hover"
      >
        <image src="../../static/icon/待评价.png" mode="scaleToFill" />
        <text class="order-name">待评价</text>
      </navigator>
      <navigator
        class="order-btn"
        url="/pages/"
        open-type="navigate"
        hover-class="navigator-hover"
      >
        <image src="../../static/icon/退款.png" mode="scaleToFill" />
        <text class="order-name">退款</text>
      </navigator>
    </view>
  </view>
  <!-- 我的宠物 -->
  <view class="my-pet">
    <!-- 标题 -->
    <view class="title">
      <text class="topic">我的宠物</text>
      <view class="more">
        <image src="../../static/icon/arrowRight.png" mode="scaleToFill" />
      </view>
    </view>
    <view class="pet-btn-list">
      <navigator
        class="pet-btn"
        url="/pages/"
        open-type="navigate"
        hover-class="navigator-hover"
      >
        <image src="../../static/images/mypet.jpg" mode="scaleToFill" />
        <view class="info">
          <text class="pet-name">护卫</text>
          <text class="pet-type">雪纳瑞 2岁</text>
        </view>
      </navigator>
      <view class="add-pet">
        <image src="../../static/icon/carbon--add-alt.png" mode="scaleToFill" />
        <text>添加宠物</text>
      </view>
    </view>
  </view>
  <scroll-view scroll-y>
    <view class="my-info-list">
    <navigator
      class="my-info"
      url="/pages/"
      open-type="navigate"
      hover-class="navigator-hover"
    >
      <view class="icon">
        <image src="../../static/icon/我的钱包.png" mode="scaleToFill" />
        <text>我的钱包</text>
      </view>
      <view class="arrow-right">
        <image src="../../static/icon/arrowRight.png" mode="scaleToFill" />
      </view>
    </navigator>
    <navigator
      class="my-info"
      url="/pages/"
      open-type="navigate"
      hover-class="navigator-hover"
    >
      <view class="icon">
        <image src="../../static/icon/地址管理.png" mode="scaleToFill" />
        <text>地址管理</text>
      </view>
      <view class="arrow-right">
        <image src="../../static/icon/arrowRight.png" mode="scaleToFill" />
      </view>
    </navigator>
    <navigator
      class="my-info"
      url="/pages/"
      open-type="navigate"
      hover-class="navigator-hover"
    >
      <view class="icon">
        <image src="../../static/icon/意见反馈.png" mode="scaleToFill" />
        <text>意见反馈</text>
      </view>
      <view class="arrow-right">
        <image src="../../static/icon/arrowRight.png" mode="scaleToFill" />
      </view>
    </navigator>
  </view>
  </scroll-view>
</template>

<style lang="scss" scoped>
.nav {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  min-height: 100rpx;
  .arrow-left {
    margin-left: 30rpx;
    image {
      width: 50rpx;
      height: 50rpx;
    }
  }

  .setting {
    margin-right: 5rpx;
    image {
      width: 60rpx;
      height: 60rpx;
      margin: 0 20rpx;
    }
  }
}
.info {
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 0 30rpx;
  margin-bottom: 30rpx;
  .avatar {
    image {
      width: 150rpx;
      height: 150rpx;
      border-radius: 50%;
    }
  }
  .intro {
    display: flex;
    flex: 1;
    flex-direction: column;
    margin: 30rpx 30rpx;
    .name {
      font-size: 40rpx;
      font-weight: bold;
      margin-bottom: 20rpx;
    }
    .desc {
      font-size: 30rpx;
      color: #ccc;
    }
  }
  .arrow-right {
    image {
      width: 60rpx;
      height: 60rpx;
      margin-right: 20rpx;
    }
  }
}
.nums {
  min-height: 80rpx;
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
  margin: 0 0 30rpx 0;
  .num {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 0 50rpx;
    text {
      margin: 0rpx 0;
    }
  }
}
.my-order {
  display: flex;
  flex-direction: column;
  .title {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 30rpx;
    margin: 10rpx 0 20rpx 0;
    .topic {
      font-size: 33rpx;
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
  .order-btn-list {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: center;
    .order-btn {
      display: flex;
      flex-direction: column;
      image {
        width: 60rpx;
        height: 60rpx;
        margin-left: 20rpx;
        margin-bottom: 10rpx;
       
      }
      .order-name {
        font-size: 30rpx;
        letter-spacing: .2rem;
       
      }
      &:nth-child(4){
         image {
          margin-left: 0;
         }
        }
    }
  }
}
.my-pet {
  display: flex;
  flex-direction: column;
  margin: 15rpx 0 10rpx 0;
  min-height: 270rpx;
  border-bottom: 1px solid #bbb;
  .title {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 30rpx;
    margin: 10rpx 0 20rpx 0;
    .topic {
      font-size: 33rpx;
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
  .pet-btn-list {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: center;

    .pet-btn {
      display: flex;
      flex-direction: row;
      image {
        width: 130rpx;
        height: 130rpx;
        border-radius: 50%;
      }
      .info {
        display: flex;
        flex-direction: column;
        .pet-name {
          font-size: large;
          color: #000;
          margin: 15rpx 0;
        }
        .pet-type {
          color: #bbb;
        }
      }
    }

    .add-pet {
      display: flex;
      flex-direction: row;
      align-items: center;
      image {
        width: 130rpx;
        height: 130rpx;
        border-radius: 50%;
      }
      text {
        margin-left: 5rpx;
        color: #bbb;
      }
    }
  }
}
.my-info-list {
  display: flex;
  flex-direction: column;
  padding: 10rpx;

  .my-info {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    min-height: 100rpx;
    .icon {
      display: flex;
      align-items:center;
      text {
        margin-left: 20rpx;
        margin-top: 20rpx;
      }
      image {
        width: 80rpx;
        height: 80rpx;
      }
    }
    .arrow-right {
      margin-top: 24rpx;
      image {
        width: 50rpx;
        height: 50rpx;
      }
    }
  }
}
</style>
