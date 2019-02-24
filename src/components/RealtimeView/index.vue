<template>
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
</template>

<script>
export default {
  name: 'RealtimeView',
  props: {
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
    }
  }
}
</script>

<style>
.spot-detail-realtime {
  padding-bottom: 20rpx;
  border-bottom: solid 2rpx #F5F3F1;
}

.spot-detail-realtime-title {
  text-align: center;
  margin-top: 30rpx;
}

.spot-detail-realtime-text {
  font-size: 28rpx;
  color: #000;
  font-weight: 800;

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
</style>
