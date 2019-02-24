<template>
<!-- 推荐目的地模块 -->
<view class="recommand">
  <!-- 模块标题 -->
  <van-cell
    title="推荐目的地"
    title-class="recommand-title"
    value="查看更多"
    value-class="recommand-value"
    custom-class="recommand-cell"
  >
    <view slot="right-icon" class="recommand-icon">
      <van-icon name="arrow" />
    </view>
  </van-cell>
  <!-- 第一排目的地 -->
  <view class="recommand-items">
    <van-row>
      <van-col>
        <a href="/pages/fake-spot/main">
          <image class="recommand-item-big" mode="scaleToFill" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/recommand1.png" />
        </a>
      </van-col>
      <van-col custom-class="recommand-item-gap">
        <image @click="comingsoon" class="recommand-item-small" mode="scaleToFill" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/recommand2.png" />
      </van-col>
    </van-row>
    <!-- 第二排目的地 -->
    <van-row custom-class="recommand-row-gap">
      <van-col>
        <image @click="comingsoon" class="recommand-item-little" mode="scaleToFill" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/recommand3.png" />
      </van-col>
      <van-col custom-class="recommand-item-gap" >
        <image @click="comingsoon" class="recommand-item-little" mode="scaleToFill" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/recommand4.png" />
      </van-col>
      <van-col custom-class="recommand-item-gap">
        <image @click="comingsoon" class="recommand-item-little" mode="scaleToFill" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/recommand5.png" />
      </van-col>
    </van-row>
  </view>
</view>
</template>

<script>
import {mapMutations} from 'vuex'
import {SET_COMINGSOON_DIALOG_SHOW} from '@/store/mutation-types'

export default {
  name: "RecommandLocation",
  methods: {
    ...mapMutations([
      SET_COMINGSOON_DIALOG_SHOW
    ]),
    comingsoon () {
      this[SET_COMINGSOON_DIALOG_SHOW](true)
    }
  }
}
</script>

<style>
.recommand {
  width: 100% !important;
  margin: 0rpx !important;
  padding: 0rpx !important;
  border-radius: 10rpx !important;
}

.recommand-cell {
  border-radius: 20rpx !important;
}

.recommand-title {
  margin-top: 30rpx;
  font-size: 36rpx;
  font-weight: 600;
  text-align: left;
}

.recommand-value {
  margin-top: 30rpx;
  font-size: 26rpx;
  color: #838386;
}

.recommand-icon {
  margin-top: 30rpx;
  font-size: 20rpx;
  color: #838386;
}

.recommand-items {
  margin-left: 25rpx;
}

.recommand-item-big {
  width: 466rpx;
  height: 270rpx;
}

.recommand-item-small {
  width: 231rpx;
  height: 270rpx;
}

.recommand-item-little {
  width: 231rpx;
  height: 158rpx;
  margin-top: -4rpx;
}

.recommand-item-gap {
  margin-left: 6rpx;
}

.recommand-row-gap {
  margin-top: 0rpx !important;
}
</style>

