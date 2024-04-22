<template>
  <!-- 头部 -->
  <view class="nav">
    <view class="router">
      <navigator
        url="/pages/"
        open-type="navigate"
        hover-class="navigator-hover"
      >
        推荐
      </navigator>
      <navigator
        url="/pages/"
        open-type="navigate"
        hover-class="navigator-hover"
      >
        关注
      </navigator>
      <navigator
        url="/pages/"
        open-type="navigate"
        hover-class="navigator-hover"
      >
        附近
      </navigator>
    </view>
    <view class="icon">
      <image src="../../static/icon/ion--search-sharp.png" mode="scaleToFill" />
      <image src="../../static/icon/message.png" mode="scaleToFill" />
      <image src="../../static/icon/camera.png" mode="scaleToFill" />
    </view>
  </view>
  <!-- 沿着X轴滚动的盒子 -->
  <scroll-view scroll-x>
    <!-- 卡片 -->
    <view class="content">
      <GuluCard>
        <template #shadow>
          <view class="shadow" style="background-color: orange"></view>
        </template>
        <template #bg>
          <image src="../static/images/宠物图1.jpeg" mode="scaleToFill" />
        </template>
        <template #title>
          <view style="display: flex; flex-direction: column">
            <text>宠物喂养</text>
            <text>注意事项</text>
          </view>
        </template>
        <template #footer>
          <text>1266人查看</text>
        </template>
      </GuluCard>
      <GuluCard>
        <template #shadow>
          <view class="shadow" style="background-color: #9999ff"></view>
        </template>
        <template #bg>
          <image src="../../static/images/宠物图2.jpg" mode="scaleToFill" />
        </template>
        <template #title>
          <view style="display: flex; flex-direction: column">
            <text>养宠攻略</text>
          </view>
        </template>
        <template #footer>
          <text>5465人查看</text>
        </template>
      </GuluCard>
      <GuluCard>
        <template #shadow>
          <view class="shadow" style="background-color: #99ffcc"></view>
        </template>
        <template #bg>
          <image src="../../static/images/宠物图3.jpg" mode="scaleToFill" />
        </template>
        <template #title>
          <view style="display: flex; flex-direction: column">
            <text>养宠科普</text>
          </view>
        </template>
        <template #footer>
          <text>8266人查看</text>
        </template>
      </GuluCard>
      <GuluCard>
        <template #shadow>
          <view class="shadow" style="background-color: hotpink"></view>
        </template>
        <template #bg>
          <image src="../../static/images/宠物图4.jpeg" mode="scaleToFill" />
        </template>
        <template #title>
          <view style="display: flex; flex-direction: column">
            <text>宠物训练</text>
          </view>
        </template>
        <template #footer>
          <text>3333人查看</text>
        </template>
      </GuluCard>
    </view>
  </scroll-view>
  <!-- 热门话题 -->
  <view class="hot-topic">
    <!-- 标题 -->
    <view class="title">
      <text class="topic">热门话题</text>
      <view class="more">
        <text>更多</text>
        <image src="../../static/icon/arrowRight.png" mode="scaleToFill" />
      </view>
    </view>
    <scroll-view scroll-y>
      <!-- 话题列表 -->
      <navigator
        class="topic-list"
        url="/pages/index"
        open-type="navigate"
        hover-class="navigator-hover"
        v-for="(topic, index) in topicList"
        :key="index"
      >
        <!-- 图片 -->
        <image :src="topic.imgUrl" mode="scaleToFill" />
        <view class="topic-detail">
          <!-- 商品名称 -->
          <text class="topic-name">{{ topic.name }}</text>
          <view>
            <view class="activity" v-if="topic.id == 1">
              <text>活动中</text>
            </view>
          </view>
          <view class="join-topic" v-if="topic.id == 1"
            >参与话题活动 发文赢大奖</view
          >
          <view class="nums">
            <text class="num">{{ topic.join_nums }}人参与</text>
          </view>
        </view>
      </navigator>
    </scroll-view>
  </view>
  <!-- 推荐关注 -->
  <view class="rec-attention">
    <!-- 标题 -->
    <view class="title">
      <text class="topic">推荐关注</text>
      <view class="more">
        <text>更多</text>
        <image src="../../static/icon/arrowRight.png" mode="scaleToFill" />
      </view>
    </view>
    <!-- 推荐列表 -->
    <navigator
      class="attention-list"
      url="/pages/index"
      open-type="navigate"
      hover-class="navigator-hover"
      v-for="(act, index) in attentionList"
      :key="index"
    >
      <!-- 图片 -->
      <image :src="act.imgUrl" mode="scaleToFill" />
      <view class="attention-detail">
        <!-- 商品名称 -->
        <text class="attention-name">{{ act.name }}</text>
        <text class="attention-fans">粉丝数 {{ act.fans }}</text>
      </view>
      <view class="attention-btn">
        <text class="attention-btn-text">关注</text>
      </view>
    </navigator>
  </view>
</template>

<script setup>
// 引入GuluCard组件 ，卡片
import GuluCard from "@/components/Gulu/GuluCard.vue";

const topicList = [
  {
    id: 1,
    name: "#萌宠出道计划",
    join_nums: 4599,
    imgUrl: "../../static/images/宠物图4.jpeg",
  },
  {
    id: 2,
    name: "#奇妙的动物",
    join_nums: 1599,
    imgUrl: "../../static/images/宠物图5.jpeg",
  },
  {
    id: 3,
    name: "#可爱的人总是发现可爱的事",
    join_nums: 1899,
    imgUrl: "../../static/images/宠物图6.jpeg",
  },
];

const attentionList = [
  {
    id: 1,
    name: "宠小兽",
    fans: "1203",
    imgUrl: "../../static/images/宠物图7.jpeg",
  },
  {
    id: 2,
    name: "酒酿熊子",
    fans: "2561",
    imgUrl: "../../static/images/宠物图8.jpeg",
  },
  {
    id: 3,
    name: "柯主任",
    fans: "3657",
    imgUrl: "../../static/images/宠物图9.jpeg",
  },
];
</script>

<style lang="scss" scoped>
.nav {
  padding: 20rpx 0 0 0;
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 0 0 30rpx 0;
  min-height: 30rpx;
  .router {
    flex: 2;
    display: flex;
    flex-direction: row;
    font-size: 35rpx;
    font-weight: bold;
    color: #001;

    navigator {
      padding: 0 30rpx;
    }
  }
  .icon {
    flex: 1;
    display: flex;
    justify-content: space-evenly;
    margin-top: 10rpx;
    image {
      width: 50rpx;
      height: 50rpx;
    }
  }
}

.shadow {
  z-index: 999;
  width: 220rpx;
  height: 250rpx;
  position: absolute;
  top: 0;
  left: 0;
  opacity: 0.8;
  border-radius: 10%;
}

.content {
  display: flex;
  flex-direction: row;
}

.hot-topic {
  display: flex;
  flex-direction: column;
  .title {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 30rpx;
    margin-top: 30rpx;
    .topic {
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
  .topic-list {
    display: flex;
    flex-direction: row;
    margin: 30rpx 30rpx;
    image {
      width: 250rpx;
      height: 200rpx;
      margin-right: 20rpx;
      border-radius: 25rpx;
    }
    .topic-detail {
      position: relative;
      display: flex;
      flex-direction: column;
      margin: 30rpx 0 0 30rpx;
      .topic-name {
        font-size: 35rpx;
        font-weight: 500;
      }
      .activity {
        position: absolute;
        top: 0;
        right: 0;
        padding: 0rpx 10rpx;
        height: 50rpx;
        text-align: center;
        border-radius: 25rpx;
        background-color: rgb(243, 163, 16);
        font-size: 30rpx;
        color: #fff;
      }
      .join-topic {
        font-size: 30rpx;
        margin: 10rpx 0;
        color: #ccc;
      }
      .nums {
        display: flex;
        justify-content: space-between;
        align-items: center;
        .num {
          margin-left: 3rpx;
          color: #bbb;
          font-size: 35rpx;
        }
      }
    }
  }
}

.rec-attention {
  display: flex;
  flex-direction: column;
  .title {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 30rpx;
    margin: 10rpx 0 20rpx 0;
    .topic {
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
  .attention-list {
    display: flex;
    align-items: center;
    flex-direction: row;
    margin: 10rpx 30rpx;
    image {
      width: 150rpx;
      height: 150rpx;
      border-radius: 50%;
      margin-right: 20rpx;
    }
    .attention-detail {
      flex: 1;
      display: flex;
      flex-direction: column;
      .attention-name {
        font-size: 35rpx;
        letter-spacing: 0.1rem;
        font-weight: bold;
      }
      .attention-fans {
        color: #ccc;
        margin-top: 10rpx;
      }
    }
    .attention-btn {
      display: flex;
      align-items: center;
      justify-content: center;
      margin-right: 50rpx;
      width: 100rpx;
      height: 50rpx;
      background-color: rgb(242, 93, 7);
      border-radius: 25rpx;
      .attention-btn-text {
        color: #fff;
        font-size: 30rpx;
      }
    }
  }
}
</style>
