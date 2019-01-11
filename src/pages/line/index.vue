<template>
<view class="container">
  <!-- 封面模块 -->
  <view>
    <image class="line-navagation-map" mode="scaleToFill" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/cover.png" />
  </view>

  <view class="line-card">
    <view class="line-card-container">
      <!-- 点位模块 -->
      <view class="spot-items">
        <lable class="spot-items-title">本攻略包含6个点位</lable>
        <van-row custom-class="spot-items-tag">
          <slide :speed="100" >
            <van-col custom-class="spot-items-tag-col">
              <van-tag custom-class="spot-item-tag">1号</van-tag>
            </van-col>
            <van-col custom-class="spot-items-tag-col">
              <van-tag custom-class="spot-item-tag spot-item-tag-gap spot-item-tag-selected">2号</van-tag>
            </van-col>
            <van-col custom-class="spot-items-tag-col">
              <van-tag custom-class="spot-item-tag spot-item-tag-gap">3号</van-tag>
            </van-col>
            <van-col custom-class="spot-items-tag-col">
              <van-tag custom-class="spot-item-tag spot-item-tag-gap">5号</van-tag>
            </van-col>
            <van-col custom-class="spot-items-tag-col">
              <van-tag custom-class="spot-item-tag spot-item-tag-gap">7号</van-tag>
            </van-col>
          </slide>
        </van-row>
      </view>

      <!-- 景点详情模块 -->
      <view class="spot-detail">
        <view class="spot-detail-title">
          <image mode="scaleToFill" class="spot-detail-title-icon" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/like.png" />
          <label class="spot-detail-title-text">梅州人家</label>
        </view>
        <view class="spot-detail-realtime">
          <view class="spot-detail-realtime-title">
            <label class="spot-detail-realtime-text">实时景观</label>
          </view>
          <view class="spot-detail-realtime-images">
            <slide :speed="100" >
              <view class="spot-detail-realtime-item">
                <image class="spot-detail-realtime-image" mode="scaleToFill" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot1.png" />
                <label class="spot-detail-realtime-time">1月6日 08:00</label>
              </view>
              <view class="spot-detail-realtime-item spot-detail-realtime-item-gap">
                <image class="spot-detail-realtime-image" mode="scaleToFill" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot2.png" />
                <label class="spot-detail-realtime-time">1月6日 13:00</label>
              </view>
              <view class="spot-detail-realtime-item spot-detail-realtime-item-gap">
                <image class="spot-detail-realtime-image" mode="scaleToFill" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot3.png" />
                <label class="spot-detail-realtime-time">1月6日 20:00</label>
              </view>
            </slide>
          </view>
        </view>
        <view class="spot-detail-desc">
          <label class="spot-detail-desc-title">地点介绍</label>
          <label class="spot-detail-desc-info">著名的旅游胜地有瑶琳仙境、桐君山、雷峰塔、岳庙、三潭映月、苏堤、六和塔、宋城、南宋御街、灵隐寺、跨湖桥遗址等。2011年6月24日，杭州西湖正式列入《世界遗产名录》。</label>
          <image class="spot-detail-desc-image" mode="scaleToFill" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot3.png" />
          <label class="spot-detail-desc-info">著名的旅游胜地有瑶琳仙境、桐君山、雷峰塔、岳庙、三潭映月、苏堤、六和塔、宋城、南宋御街、灵隐寺、跨湖桥遗址等。2011年6月24日，杭州西湖正式列入《世界遗产名录》。著名的旅游胜地有瑶琳仙境等。</label>
        </view>
      </view>
    </view>
  </view>
  
</view>
</template>

<script>
import slide from 'mpvue-slide'

export default {
  data() {
    return {
    }
  },
  methods: {
  },
  components: {
    slide
  }
}
</script>

<style>
.container {
  width: 750rpx !important;
  height: 100%;
  text-align: center;
  display: block;
  align-items: center;
  justify-content: center;
}

.line-navagation-map {
  width: 100%;
  height: 854rpx;
}

.line-card-container {
  margin-left: 30rpx;
  padding: 0 !important;
  margin-top: 0 !important;
}

.spot-items {
  text-align: left;
}

.spot-items-title {
  font-size: 25rpx;
  font-weight: 400;
  color: #838386;
}

.spot-items-tag {
  margin-right: 0 !important;
  display: inline;
  white-space: nowrap; 
  overflow: hidden;
}

.spot-item-tag {
  width: 136rpx;
  height: 60rpx;
  padding: 0 !important;
  display: flex !important;
  align-items: center;
  justify-content: center; 
  border-radius: 8rpx !important;
  background-color: #EEF1F6 !important;
  color: #838386 !important;
  margin-top: 15rpx;
  font-size: 25rpx !important;
}

.spot-items-tag-col {
  display: inline-block;
}

.spot-item-tag-gap {
  margin-left: 18rpx;
}

.spot-item-tag-selected {
  background-color: #EAEDF4 !important;
  color: #28272C !important;
  font-weight: 600;
}

.spot-detail-title {
  text-align: left;
  margin-top: 50rpx;
}

.spot-detail-title-icon {
  width: 50rpx;
  height: 60rpx;
}

.spot-detail-title-text {
  position: relative;
  top: -12rpx;
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
  width: 252rpx;
  height: 180rpx;
}

.spot-detail-realtime-image-gap {
  margin-left: 20rpx;
}

.spot-detail-realtime-times {
  text-align: left;
}

.spot-detail-realtime-item {
  width: 252rpx;
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
}

.spot-detail-desc-image {
  margin-top: 40rpx;
  width: 686rpx;
  height: 424rpx;
}

</style>
