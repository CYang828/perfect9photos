<template>
<!-- 评论模块 -->
<view>
  <!-- 模块标题 -->
  <van-cell
    title="推荐目的地"
    title-class="comment-title"
    value="查看更多"
    value-class="comment-value"
    v-bind:border="false"
  >
    <view slot="right-icon" class="comment-icon">
      <van-icon name="arrow" />
    </view>
  </van-cell>

  <view class="comment-item">
    <view>
      <van-cell 
        custom-class="comment-head" 
        center
        v-bind:border="false"> 
        <view slot="title">
          <van-row>
            <van-col>
              <image class="comment-avator" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/avator1.png" />
            </van-col>
            <van-col custom-class="comment-head-title">
              <van-row>
                <label class="comment-head-username">花花</label>
              </van-row>
              <van-row>
                <label class="comment-head-time">今天 12:42</label>
              </van-row>
            </van-col>
            <van-col>
              <van-cell 
              custom-class="comment-head-like-cell" 
              title-class="comment-head-like"
              v-bind:border="false">
                <view slot="title">
                  <image src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/heart.png" class="comment-head-like-icon" />
                  <label class="comment-head-like-count">796</label>
                </view>
              </van-cell>
            </van-col>
          </van-row>
        </view>
      </van-cell>
      <view class="comment-images">
        <van-row custom-class="comment-image-row-gap">
          <van-col>
            <image src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment1-1.png" mode="scaleToFill" class="comment-image" />
          </van-col>
          <van-col custom-class="comment-image-gap">
            <image src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment1-2.png" mode="scaleToFill" class="comment-image" />
          </van-col>
          <van-col custom-class="comment-image-gap">
            <image src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment1-3.png" mode="scaleToFill" class="comment-image" />
          </van-col>
        </van-row>
        <van-row custom-class="comment-image-row-gap">
          <van-col>
            <image src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment1-4.png" mode="scaleToFill" class="comment-image" />
          </van-col>
          <van-col custom-class="comment-image-gap">
            <image src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment1-5.png" mode="scaleToFill" class="comment-image" />
          </van-col>
          <van-col custom-class="comment-image-gap">
            <image src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment1-6.png" mode="scaleToFill" class="comment-image" />
          </van-col>      
        </van-row>
        <van-row custom-class="comment-image-row-gap">
          <van-col>
            <image src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment1-7.png" mode="scaleToFill" class="comment-image" />
          </van-col>
          <van-col custom-class="comment-image-gap">
            <image src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment1-8.png" mode="scaleToFill" class="comment-image" />
          </van-col>
          <van-col custom-class="comment-image-gap">
            <image src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment1-9.png" mode="scaleToFill" class="comment-image" />
          </van-col>      
        </van-row>
        <van-row custom-class="comment-text">
          <label>
            这是一次意料之外的旅行，也收获了意料之外的惊喜。在做攻略时就彻底被土耳其折服了，充满历史厚重感的伊斯坦布尔，漫天热气球的卡…
          </label>
        </van-row>
        <van-row>
          <van-cell 
          custom-class="comment-location-cell">
            <view slot="title">
              <van-tag custom-class="comment-location-tag" color="#EEF1F6">
                <image class="comment-location-tag-icon" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/location.png" />
                <lable class="comment-location-tag-text">开塞利</lable>
              </van-tag>
              <van-tag plain round custom-class="comment-map-navigation">
                <image src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/plane.png" class="comment-map-navigation-icon" />
                <label class="comment-map-navigation-text">去这里</label>
              </van-tag>
            </view>
          </van-cell>
        </van-row>
      </view>
    </view>
  </view>

  <view class="comment-item">
    <van-cell 
      custom-class="comment-head" 
      center> 
      <view slot="title">
        <van-row>
          <van-col>
            <image class="comment-avator" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/avator1.png" />
          </van-col>
          <van-col custom-class="comment-head-title">
            <van-row>
              <label class="comment-head-username">花花</label>
            </van-row>
            <van-row>
              <label class="comment-head-time">今天 12:42</label>
            </van-row>
          </van-col>
          <van-col>
            <van-cell 
            custom-class="comment-head-like-cell" 
            title-class="comment-head-like">
              <view slot="title">
                <image src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/heart.png" class="comment-head-like-icon" />
                <label class="comment-head-like-count">230</label>
              </view>
            </van-cell>
          </van-col>
        </van-row>
      </view>
    </van-cell>
    <view class="comment-images">
      <van-row custom-class="comment-image-row-gap">
        <van-col>
          <image src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment1-1.png" mode="scaleToFill" class="comment-image" />
        </van-col>
        <van-col custom-class="comment-image-gap">
          <image src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment1-2.png" mode="scaleToFill" class="comment-image" />
        </van-col>
        <van-col custom-class="comment-image-gap">
          <image src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment1-3.png" mode="scaleToFill" class="comment-image" />
        </van-col>
      </van-row>
      <van-row custom-class="comment-text">
          <label>
            这是一次意料之外的旅行，也收获了意料之外的惊喜。在做攻略时就彻底被土耳其折服了，充满历史厚重感的伊斯坦布尔，漫天热气球的卡…
          </label>
        </van-row>
        <van-row>
          <van-cell 
          custom-class="comment-location-cell"
          v-bind:border="false">
            <view slot="title">
              <van-tag custom-class="comment-location-tag" color="#EEF1F6">
                <image class="comment-location-tag-icon" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/location.png" />
                <lable class="comment-location-tag-text">开塞利</lable>
              </van-tag>
              <van-tag plain round custom-class="comment-map-navigation">
                <image src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/plane.png" class="comment-map-navigation-icon" />
                <label class="comment-map-navigation-text">去这里</label>
              </van-tag>
            </view>
          </van-cell>
        </van-row>
    </view>
  </view>
</view>
</template>

<script>
export default {
  name: "UserComment"
}
</script>

<style>
.comment {
  width: 750rpx !important;
  margin: 0rpx !important;
  padding: 0rpx !important;
}

.comment-item + .comment-item {
  margin-top: 30rpx;
}

.comment-title {
  margin-top: 30rpx;
  margin-bottom: 30rpx;
  font-size: 36rpx;
  font-weight: 600;
  text-align: left;
}

.comment-value {
  margin-top: 30rpx;
  font-size: 26rpx;
  color: #838386;
}

.comment-icon {
  margin-top: 30rpx;
  font-size: 20rpx;
  color: #838386;
}

.comment-avator {
  border-radius: 50%;
  width: 68rpx !important;
  height: 68rpx !important;
}

.comment-head {
  text-align: left;
  padding: 0rpx 30rpx !important;
}

.comment-head-title {
  margin-top: -4rpx;
  margin-left: 8rpx;
}

.comment-head-username {
  font-size: 14px;
  font-weight: 600;
}

.comment-head-time {
  position: relative;
  top: -14rpx;
  font-size: 10px;
  color: #838386;
}

.comment-head-like-cell {
  padding: 10rpx 0rpx 0rpx 0rpx !important; 
  margin-left: 420rpx;
}

.comment-head-like-icon {
  width: 36rpx;
  height: 36rpx;
}

.comment-head-like-count {
  position: relative;
  top: -6rpx;
  margin-left: 8rpx;
  font-size: 28rpx;
  font-weight: 600;
  color: #28272C;
}

.comment-images {
  margin-left: 108rpx;
  margin-top: 0rpx;
  padding: 0rpx;
}

.comment-image {
  width: 198rpx;
  height: 198rpx;
  margin-top: -5rpx;
}

.comment-image-gap {
  margin-left: 6rpx;
}

.comment-image-row-gap {
  margin-top: 0rpx !important;

}

.comment-text {
  margin-top: 10rpx;
  padding-right: 28rpx !important;
  text-align: left;
  font-size: 29rpx;
}

.comment-location-cell {
  width: auto !important;
  margin-top: 20rpx;
  margin-right: 38rpx;
  padding: 0 0 30rpx 0 !important;
  text-align: left;
  border-bottom: solid 2rpx #F5F3F1;
}

.comment-location-tag {
  color: #28272C;
  padding: .45em .45em 0 .45em !important;
}

.comment-location-tag-icon {
  width: 30rpx;
  height: 30rpx;
}

.comment-location-tag-text {
  position: relative;
  top: -8rpx;
  color: #28272C;
  font-weight: 500;
  font-size: 20rpx;
  margin-left: 6rpx;
}

.comment-map-navigation {
  margin-left: 360rpx;
  padding: .45em .45em 0 .45em !important;
}

.comment-map-navigation-icon {
  width: 30rpx;
  height: 22rpx;
}

.comment-map-navigation-text {
  position: relative;
  font-size: 22rpx;
  margin-left: 6rpx;
  top: -4rpx;
  color: #2D2D30;
}
</style>

