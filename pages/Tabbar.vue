<template>
  <view>
    <view class="u-page">
      <!-- 所有内容的容器 -->
      <view class="" v-for="(item,index) in list" :key="index">
        <image :src="item.iconPath" mode=""></image>
      </view>
    </view>
    <!-- 与包裹页面所有内容的元素u-page同级，且在它的下方 -->
    <u-tabbar v-model="current" :list="list" :mid-button="true"></u-tabbar>
  </view>
</template>

<script>
  export default {
    data() {
      return {
        list: [{
            iconPath: "home",
            selectedIconPath: "home-fill",
            text: '首页',
            count: 2,
            isDot: true,
            customIcon: false,
          },
          {
            iconPath: "photo",
            selectedIconPath: "photo-fill",
            text: '放映厅',
            customIcon: false,
          },
          {
            iconPath: "play-right",
            selectedIconPath: "play-right-fill",
            text: '直播',
            customIcon: false,
          },
          {
            iconPath: "account",
            selectedIconPath: "account-fill",
            text: '我的',
            count: 23,
            isDot: false,
            customIcon: false,
          },
        ],
        current: 0
      }
    },
  }
</script>