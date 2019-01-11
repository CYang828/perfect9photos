<template>
  <view class="container">
    <!-- 封面模块 -->
    <view>
      <image class="cover-image" mode="scaleToFill" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/cover.png" />
      <view class="location">
        <van-cell custom-class="location-cell" v-bind:border="false" center>
          <view slot="title">
            <label class="location-name">北京</label>
            <van-icon custom-class="heart-icon" name="like" />
          </view>
        </van-cell>
        <van-cell custom-class="location-cell" v-bind:border="false" center>
          <view slot="title" class="align">
            <image class="sun-icon" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/sun.png" />
            <label class="temperature">25°</label>
          </view>
        </van-cell>
      </view>
      <van-search custom-class="search" background="#fff" placeholder-class="search-placeholder" maxlength="50" placeholder="请输入目的地" />
    </view>

    <view class="card-border">

      <recommand-location />
      <user-comment />
    </view>
  </view>
</template>

<script>
import RecommandLocation from '@/components/RecommandLocation/index.vue'
import UserComment from '@/components/UserComment/index.vue'

export default {
  data () {
    return {}
  },
  components: {
    RecommandLocation,
    UserComment
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

.cover-image {
  width: 100%;
  height: 804rpx;
}
.align {
  display: flex;
}
.location {
  position: absolute;  
  top: 326rpx;
  opacity: 0.95;
  z-index: 999;
  margin-left: 33%;
}

.location-cell {
  padding: 6rpx 30rpx !important;
  background-color: transparent !important;
}

.location-name {
  padding-left: 40rpx;
  font-size: 52rpx;
  font-weight: 600;
  color: #fff;
}

.heart-icon {
  margin-left: 10rpx;
  font-size: 20rpx !important;
  color: #fff;
}

.sun-icon {
  width: 50rpx;
  height: 50rpx;
  opacity: 95%;
  padding-left: 40rpx;
}

.temperature {
  color: #fff;
  font-size: 30rpx;
  font-weight: 500;
  margin-left: 10rpx; 
  margin-top: 2rpx;
}

.search {
  position: absolute;  
  top: 636rpx;  
  left: 5%;
  width: 90%;
  height: 84rpx;
  opacity: 0.95;
  z-index: 999;
  border-radius:60rpx;
}

.van-search__field {
  margin-left: 30%;
}

.card-border {
  position: absolute;
  border-radius: 60rpx;
  top: 790rpx;
  z-index: 998;
  background-color: #fff;
}
</style>
