<template>
  <!-- 景点详情模块 -->
  <view>
    <view class="spot-detail">
      <view class="spot-detail-title">
        <image mode="scaleToFill" 
        class="spot-detail-title-icon" 
        src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/like.png" />
        <label class="spot-detail-title-text">{{title}}</label>
      </view>
      <view class="spot-detail-realtime">
        <view class="spot-detail-realtime-title">
          <label class="spot-detail-realtime-text">实时景观</label>
        </view>
        <view class="spot-detail-realtime-images">
        <van-row>
          <van-col>
            <view class="spot-detail-realtime-item">
              <image class="spot-detail-realtime-image" 
              mode="scaleToFill" 
              :src="viewImage1" />
              <label class="spot-detail-realtime-time">{{viewImage1Time}}</label>
            </view>
          </van-col>
          <van-col>
            <view class="spot-detail-realtime-item spot-detail-realtime-item-gap">
              <image class="spot-detail-realtime-image" 
              mode="scaleToFill" 
              :src="viewImage2" />
              <label class="spot-detail-realtime-time">{{viewImage2Time}}</label>
            </view>
          </van-col>
          <van-col>
            <view class="spot-detail-realtime-item spot-detail-realtime-item-gap">
              <image class="spot-detail-realtime-image" 
              mode="scaleToFill" 
              :src="viewImage3" />
              <label class="spot-detail-realtime-time">{{viewImage3Time}}</label>
            </view>
          </van-col>
        </van-row>
        </view>
      </view>
      <view class="spot-detail-desc">
        <label class="spot-detail-desc-title">地点介绍</label>
        <label class="spot-detail-desc-info">{{info}}</label>
        <image class="spot-detail-desc-image" mode="scaleToFill" :src="image" />
        <label class="spot-detail-desc-info">{{address}}</label>
        <label class="spot-detail-desc-info">{{price}}</label>
        <label class="spot-detail-desc-info">{{phone}}</label>
        <label class="spot-detail-desc-info">{{way}}</label>
        <label class="spot-detail-desc-info">{{open}}</label>
      </view>
    </view>
  </view>
</template>

<script>
import slide from '@/components/mpvue-slide/mpvue-slide.vue'

export default {
  name: "SpotDetail",
  components: {
    slide,
  },
  props: {
    "title": {
      type: String
    },
    "viewImage1": {
      type: String
    },
    "viewImage1Time": {
      type: String
    },
    "viewImage2": {
      type: String
    },
    "viewImage2Time": {
      type: String
    },
    "viewImage3": {
      type: String
    },
    "viewImage3Time": {
      type: String
    },
    "info": {
      type: String
    },
    "image": {
      type: String
    },
    "detail": {
      type: String
    },
    "address": {
      type: String
    },
    "price": {
      type: String
    },
    "phone": {
      type: String
    },
    "way": {
      type: String
    },
    "open": {
      type: String
    }
  }
}
</script>

<style>
.spot-detail-title {
  text-align: left;
  margin-top: 50rpx;
}

.spot-detail-title-icon {
  width: 50rpx;
  height: 57rpx;
}

.spot-detail-title-text {
  position: relative;
  top: -10rpx;
  margin-left: 8rpx;
  font-size: 55rpx;
  font-weight: 800;
}

.spot-detail-realtime {
  padding-bottom: 20rpx;
  border-bottom: solid 2rpx #F5F3F1;
}

.spot-detail-realtime-title {
  text-align: left;
  margin-top: 30rpx;
}

.spot-detail-realtime-text {
  font-size: 40rpx;
  font-weight: 500;
}

.spot-detail-realtime-images {
  margin-top: 30rpx;
}

.spot-detail-realtime-image {
  display: inline-block;
  width: 220rpx;
  height: 180rpx;
}

.spot-detail-realtime-image-gap {
  margin-left: 20rpx;
}

.spot-detail-realtime-times {
  text-align: left;
}

.spot-detail-realtime-item {
  width: 220rpx;
  text-align: left;
}

.spot-detail-realtime-item-gap {
  margin-left: 20rpx;
}

.spot-detail-realtime-time {
  color: #838386;
  font-size: 24rpx;
  position: relative;
  top: -10rpx;
}

.spot-detail-realtime-time-gap {
  margin-left: 30rpx;
}

.spot-detail-desc {
  text-align: left;
  margin-top: 40rpx;
  margin-right: 30rpx;
}

.spot-detail-desc-title {
  font-size: 40rpx;
  font-weight: 500;
  display: block;
}

.spot-detail-desc-info {
  display: block;
  margin-top: 30rpx;
  text-align: left;
  font-size: 24rpx;
  color: #838386;
  font-weight: 400;
  letter-spacing: -1rpx;;
}

.spot-detail-desc-image {
  margin-top: 40rpx;
  width: 686rpx;
  height: 424rpx;
}
</style>
