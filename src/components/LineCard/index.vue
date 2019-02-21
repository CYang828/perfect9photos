<template>
<view>
  <a :href="href">  
    <image class="line-item-image" :src="image" />
  </a>
  <lable class="line-item-desc-title">{{ title }}</lable>
  <label class="line-item-desc-info">{{ info }}</label>
  <view class="line-item-desc-footer">
    <image class="line-item-desc-like" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/like.png" />
    <label class="line-item-desc-like-count">{{ like_count }}</label>
    <image class="line-item-desc-hotism" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/hot.png" />
    <label class="line-item-desc-hotism-count">{{ hotism_count }}</label>
  </view>
</view>
</template>

<script>
export default {
  name: "LineCard",
  props: {
    'href': {
      type: String,
      default: '#'
    },
    'image': {
      type: String
    },
    'title': {
      type: String
    },
    'info': {
      type: String
    },
    'like_count': {
      type: Number
    },
    'hotism_count': {
      type: Number
    }
  }
}
</script>

<style>
.line-item-image {
  width: 330rpx;
  height: 230rpx;
}

.line-item-desc-title {
  display: block !important;
  margin-left: 20rpx;
  font-size: 30rpx;
  font-weight: 500;
}

.line-item-desc-info {
  margin-left: 20rpx;
  font-size: 26rpx;
  color: #838386;
}

.line-item-desc-footer {
  margin-top: 35rpx;
  margin-left: 125rpx;
}

.line-item-desc-like {
  width: 28rpx;
  height: 32rpx;
}

.line-item-desc-like-count {
  font-size: 28rpx;
  position: relative;
  top: -4rpx;
  margin-left: 4rpx;
  font-weight: 500;
}

.line-item-desc-hotism {
  margin-left: 30rpx;
  width: 28rpx;
  height: 32rpx;
}

.line-item-desc-hotism-count {
  font-size: 28rpx;
  position: relative;
  top: -4rpx;
  margin-left: 4rpx;
  font-weight: 500;
}
</style>
