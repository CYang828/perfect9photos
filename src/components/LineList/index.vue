<template>
<!-- 路线列表 -->
<view class="line-items">
  <view class="line-items-head">
    <label class="line-items-head-text">九图攻略</label>
  </view>
  <!-- 过滤器 -->
  <view class="line-items-filter">
    <van-row>
      <van-col>
        <view class="dropdown">
          <view class="line-items-filter-condition">
            <span class="line-items-filter-text">{{ filter1_name }}</span>
            <image class="arrow-down" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/arrow-down-gray.png" />
          </view>
          <view class="dropdown-content">
            <label v-for="(item, index) in filter1" :key="index" 
            @click="onFilter1Select(event, index)" 
            :class="{ 'dropdown-selected':index==filter1SelectedIndex }">{{ item }}</label>
          </view>
        </view>
      </van-col>
      <van-col>
        <view class="dropdown">
          <view class="line-items-filter-condition">
            <span class="line-items-filter-text line-items-filter-gap">综合排序</span>
            <image class="arrow-down" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/arrow-down-gray.png" />
          </view>
          <view class="dropdown-content">
            <label v-for="(item, index) in filter2" :key="index" 
            @click="onFilter2Select(event, index)" 
            :class="{ 'dropdown-selected':index==filter2SelectedIndex }">{{ item }}</label>
          </view>
        </view>
      </van-col>
      <van-col>
        <view class="dropdown">
          <view>
            <label class="line-items-filter-text line-items-filter-gap">所有时间</label>
            <image class="arrow-down" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/arrow-down-gray.png" />
          </view>
          <view class="dropdown-content">
            <label v-for="(item, index) in filter3" :key="index" 
            @click="onFilter3Select(event, index)" 
            :class="{ 'dropdown-selected':index==filter3SelectedIndex }">{{ item }}</label>
          </view>
        </view>
      </van-col>
    </van-row>
  </view>
  
  <!-- 路线item -->
  <view>
    <van-row v-for="idx in lineRow" :key="idx" custom-class="line-item-row-gap">
      <van-col custom-class="line-item">
        <line-card 
        :href="lines[2*idx-2].href"
        :image="lines[2*idx-2].image"
        :title="lines[2*idx-2].title"
        :info="lines[2*idx-2].info"
        :like_count="lines[2*idx-2].like_count"
        :hotism_count="lines[2*idx-2].hotism_count" />
      </van-col>
      <van-col custom-class="line-item line-item-gap">
        <line-card 
        :href="lines[2*idx-1].href"
        :image="lines[2*idx-1].image"
        :title="lines[2*idx-1].title"
        :info="lines[2*idx-1].info"
        :like_count="lines[2*idx-1].like_count"
        :hotism_count="lines[2*idx-1].hotism_count" />
      </van-col>
    </van-row>
  </view>
</view>
</template>

<script>
import LineCard from '@/components/LineCard/index.vue'

export default {
  name: "LineList",
  data () {
    return {
      lineRow: 4,
      filter1SelectedIndex: 0,
      filter2SelectedIndex: 0,
      filter3SelectedIndex: 0,
      filter1: ['全部路线', '美食路线', '民宿路线', '自驾路线'],
      filter2: ['综合排序', '评价最多', '预算低到高', '预算高到低'],
      filter3: ['所有时间', '一日游', '三日游', '十日游'],
      filter1_name: '全部路线',
      filter2_name: '综合排序',
      filter3_name: '所有时间',
      linesRow: 3,
      lines: [{
        href: "/pages/line/main",
        image: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/line1.png",
        title: "梅州老字号美食推荐",
        info: "百家传承，客家味道！",
        like_count: 29,
        hotism_count: 2068
      },
      {
        href: "#",
        image: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/line2.png",
        title: "梅州特色美食之旅",
        info: "地道梅州味",
        like_count: 26,
        hotism_count: 2014
      },
      {
        href: "#",
        image: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/line3.png",
        title: "尝遍客家美食，客家米饭香",
        info: "预算2000，吃货福利！",
        like_count: 5,
        hotism_count: 1386
      },
      {
        href: "#",
        image: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/line4.png",
        title: "精品农家乐推荐",
        info: "享地道美食，品纯粹生活",
        like_count: 4,
        hotism_count: 1025
      },
      {
        href: "#",
        image: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/line5.png",
        title: "传统客家民宿",
        info: "全身心拥抱客家文化",
        like_count: 8,
        hotism_count: 2706
      },
      {
        href: "#",
        image: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/line6.png",
        title: "风光观景民宿推荐",
        info: "远离繁华地，梦入桃花源",
        like_count: 4,
        hotism_count: 3760
      },
      {
        href: "#",
        image: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/line7.png",
        title: "一天赏遍梅州景",
        info: "邂逅难忘的梅州风光",
        like_count: 7,
        hotism_count: 3265
      },
      {
        href: "#",
        image: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/line8.png",
        title: "深入领略客家文化",
        info: "文化深厚，不虚此行",
        like_count: 12,
        hotism_count: 1128
      },],
      line_data: null,
    }
  },
  components: {
    LineCard
  },
  methods: {
    onFilter1Select (event, index) {
      this.filter1SelectedIndex = index
      this.filter1_name = this.filter1[index]

      if (this.lineRow == 4) {
        this.line_data = this.lines.slice(0)
      }

      if (index == 0) {
        this.lineRow = 4
        this.lines = this.line_data.slice(0)
      }
      else if (index == 1) {
        this.lines = this.line_data.slice(0)
        this.lineRow = 2
        this.lines.splice(5, 7)
      }
      else if (index == 2) {
        this.lines = this.line_data.slice(0)
        this.lineRow = 1
        this.lines.splice(0, 4)
      }
      else if (index == 3) {
        this.lines = this.line_data.slice(0)
        this.lineRow = 1
        this.lines.splice(0, 6)
      }
    },
    onFilter2Select (event, index) {
      this.filter2SelectedIndex = index
      this.filter2_name = this.filter2[index]
    },
    onFilter3Select (event, index) {
      this.filter3SelectedIndex = index
      this.filter3_name = this.filter3[index]
    },
  }
}
</script>

<style>
.line-items {
  margin-top: 40rpx;
  text-align: left;
  margin-left: 30rpx;
  margin-right: 30rpx;
}

.line-items-head-text {
  text-align: left;
  font-size: 36rpx;
  font-weight: 600;
}

.line-items-filter {
  margin-top: 40rpx;
  margin-left: 50rpx;
  padding-bottom: 20rpx;
}

.line-items-filter-condition {
  padding-right: 20rpx;
  border-right: solid 2rpx #F5F3F1;
}

.line-items-filter-text {
  margin-right: 34rpx;
  font-size: 30rpx;
  color: #838386;
  font-weight: 450;
}

.arrow-down {
  width: 20rpx;
  height: 10rpx;
  position: relative;
  top: -4rpx;
}

.line-items-filter-gap {
  margin-left: 20rpx;
}

.line-items-filter-selected {
  color: #000;
}

.line-item {
  width: 333rpx;
  border: solid 1rpx #F2F0ED;
  border-radius: 14rpx;
}

.line-item-gap {
  margin-left: 20rpx;
}

.line-item-row-gap {
  margin-top: 20rpx;
}

.user-action {
  vertical-align:middle;
}

.card-thumb {
  width: 180px !important;
  height: 100px !important;
  border-radius: 15px;
}

.van-card__content {
  margin-left: 70px;
}

.dropdown-content {
  display:none;
  position:absolute;
  background-color:#EEEEEE;
  width:200rpx;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
}

.dropdown-content label {
    display:block;
    text-decoration:none;
    color:black;
    padding:2rpx 40rpx;
    font-size: 24rpx;
}
/*注意这里不是.dropbtn:hover，因为dropbtn是一个button,不能够用hover*/
.dropdown:hover .dropdown-content {
    display:block;
}
.dropdown-content label:hover {
    background-color:#DDDDDD;
}

.dropdown-selected {
  font-weight: 700;
}
</style>
