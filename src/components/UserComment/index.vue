<template>
<!-- 评论模块 -->
<view>
  <!-- 模块标题 -->
  <van-cell
    title="热门九图客"
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
        v-bind:border="false"> 
        <view slot="title">
          <van-row>
            <van-col>
              <image class="comment-avator" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/avator1.png" />
            </van-col>
            <van-col custom-class="comment-head-title">
              <van-row>
                <label class="comment-head-username">摄影师小涂</label>
              </van-row>
              <van-row>
                <label class="comment-head-time">今天 12:42</label>
              </van-row>
            </van-col>
            <van-col>
              <view class="comment-head-like">
                <image src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/heart.png" class="comment-head-like-icon" />
                <label class="comment-head-like-count">925</label>
              </view>
            </van-col>
          </van-row>
        </view>
      </van-cell>
      <view class="comment-images">
        <van-row custom-class="comment-image-row-gap">
          <van-col>
            <image @click="onPreview" id="1-1" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment1-1.png" mode="scaleToFill" class="comment-image" />
          </van-col>
          <van-col custom-class="comment-image-gap">
            <image @click="onPreview" id="1-2" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment1-2.png" mode="scaleToFill" class="comment-image" />
          </van-col>
          <van-col custom-class="comment-image-gap">
            <image @click="onPreview" id="1-3" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment1-3.png" mode="scaleToFill" class="comment-image" />
          </van-col>
        </van-row>
        <van-row custom-class="comment-image-row-gap">
          <van-col>
            <image @click="onPreview" id="1-4" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment1-4.png" mode="scaleToFill" class="comment-image" />
          </van-col>
          <van-col custom-class="comment-image-gap">
            <image @click="onPreview" id="1-5" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment1-5.png" mode="scaleToFill" class="comment-image" />
          </van-col>
          <van-col custom-class="comment-image-gap">
            <image @click="onPreview" id="1-6" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment1-6.png" mode="scaleToFill" class="comment-image" />
          </van-col>      
        </van-row>
        <van-row custom-class="comment-image-row-gap">
          <van-col>
            <image @click="onPreview" id="1-7" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment1-7.png" mode="scaleToFill" class="comment-image" />
          </van-col>
          <van-col custom-class="comment-image-gap">
            <image @click="onPreview" id="1-8" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment1-8.png" mode="scaleToFill" class="comment-image" />
          </van-col>
          <van-col custom-class="comment-image-gap">
            <image @click="onPreview" id="1-9" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment1-9.png" mode="scaleToFill" class="comment-image" />
          </van-col>      
        </van-row>
        <van-row custom-class="comment-text">
          <label>
            喜看稻菽千重浪，又是一年丰收时。夕阳西下，漫步在大埔县西河镇车龙村，不时能看到菜地里忙碌的村民，放眼望去是大片的金色稻浪。
          </label>
        </van-row>
        <van-row>
          <van-cell 
          custom-class="comment-location-cell"
          v-bind:border="false">
            <view slot="title">
              <van-tag custom-class="comment-location-tag" color="#EEF1F6">
                <image class="comment-location-tag-icon" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/location.png" />
                <lable class="comment-location-tag-text">梅州</lable>
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
      center
      v-bind:border="false"> 
      <view slot="title">
        <van-row>
          <van-col>
            <image class="comment-avator" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/avator2.png" />
          </van-col>
          <van-col custom-class="comment-head-title">
            <van-row>
              <label class="comment-head-username">花花</label>
            </van-row>
            <van-row>
              <label class="comment-head-time">昨天 20:42</label>
            </van-row>
          </van-col>
          <van-col>
            <view class="comment-head-like">
              <image src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/heart.png" class="comment-head-like-icon" />
              <label class="comment-head-like-count">825</label>
            </view>
          </van-col>
        </van-row>
      </view>
    </van-cell>
    <view class="comment-images">
      <van-row custom-class="comment-image-row-gap">
        <van-col>
          <image @click="onPreview" id="2-1" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment2-1.png" mode="scaleToFill" class="comment-image" />
        </van-col>
        <van-col custom-class="comment-image-gap">
          <image @click="onPreview" id="2-2" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment2-2.png" mode="scaleToFill" class="comment-image" />
        </van-col>
        <van-col custom-class="comment-image-gap">
          <image @click="onPreview" id="2-3" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment2-3.png" mode="scaleToFill" class="comment-image" />
        </van-col>
      </van-row>
      <van-row custom-class="comment-text">
          <label>
            食在广州 ，厨出凤城 。这里的凤城就指顺德，顺德是粤菜的发源地。正宗粤菜，寻味顺德。对于吃货来说，风景其次，美食才是王道。
          </label>
        </van-row>
        <van-row>
          <van-cell 
          custom-class="comment-location-cell"
          v-bind:border="false">
            <view slot="title">
              <van-tag custom-class="comment-location-tag" color="#EEF1F6">
                <image class="comment-location-tag-icon" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/location.png" />
                <lable class="comment-location-tag-text">顺德</lable>
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

  <view class="comment-item">
    <view>
      <van-cell 
        custom-class="comment-head" 
        v-bind:border="false"> 
        <view slot="title">
          <van-row>
            <van-col>
              <image class="comment-avator" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/avator3.png" />
            </van-col>
            <van-col custom-class="comment-head-title">
              <van-row>
                <label class="comment-head-username">爱旅行的千纸鹤</label>
              </van-row>
              <van-row>
                <label class="comment-head-time">18-08 09:40</label>
              </van-row>
            </van-col>
            <van-col>
              <view class="comment-head-like">
                <image src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/heart.png" class="comment-head-like-icon" />
                <label class="comment-head-like-count">674</label>
              </view>
            </van-col>
          </van-row>
        </view>
      </van-cell>
      <view class="comment-images">
        <van-row custom-class="comment-image-row-gap">
          <van-col>
            <image @click="onPreview" id="3-1" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment3-1.png" mode="scaleToFill" class="comment-image" />
          </van-col>
          <van-col custom-class="comment-image-gap">
            <image @click="onPreview" id="3-2" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment3-2.png" mode="scaleToFill" class="comment-image" />
          </van-col>
          <van-col custom-class="comment-image-gap">
            <image @click="onPreview" id="3-3" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment3-3.png" mode="scaleToFill" class="comment-image" />
          </van-col>
        </van-row>
        <van-row custom-class="comment-image-row-gap">
          <van-col>
            <image @click="onPreview" id="3-4" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment3-4.png" mode="scaleToFill" class="comment-image" />
          </van-col>
          <van-col custom-class="comment-image-gap">
            <image @click="onPreview" id="3-5" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment3-5.png" mode="scaleToFill" class="comment-image" />
          </van-col>
          <van-col custom-class="comment-image-gap">
            <image @click="onPreview" id="3-6" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment3-6.png" mode="scaleToFill" class="comment-image" />
          </van-col>      
        </van-row>
        <van-row custom-class="comment-text">
          <label>
            “停车坐爱枫林晚，霜叶红于二月花”十月的天越来越凉，正是赏红叶拍红林的最佳时节。金秋留坝是赏红叶的自驾胜地，强烈推荐！
          </label>
        </van-row>
        <van-row>
          <van-cell 
          custom-class="comment-location-cell"
          v-bind:border="false">
            <view slot="title">
              <van-tag custom-class="comment-location-tag" color="#EEF1F6">
                <image class="comment-location-tag-icon" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/location.png" />
                <lable class="comment-location-tag-text">留坝</lable>
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
</view>
</template>

<script>
export default {
  name: "UserComment",
  methods: {
    onPreview (event) {
      const imageUrl = "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/comment" + event.target.id + ".png"
      wx.previewImage({urls: [imageUrl], current: imageUrl})
    }
  }
}
</script>

<style>
.comment {
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

.comment-head-like {
  position:absolute;
  right:0px;  
  margin-right: 30rpx;
  margin-top: 10rpx;
}

.comment-head-like-icon {
  width: 36rpx;
  height: 32rpx;
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
  width: 20rpx;
  height: 28rpx;
}

.comment-location-tag-text {
  position: relative;
  top: -5rpx;
  color: #28272C;
  font-weight: 500;
  font-size: 20rpx;
  margin-left: 6rpx;
}

.comment-map-navigation {
  margin-left: 405rpx;
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

