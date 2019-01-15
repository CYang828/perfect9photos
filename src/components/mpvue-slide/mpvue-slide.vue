<style>
  .mpvue-slide {
    position: relative;
    overflow: hidden;
    z-index: 1;
  }
  .mpvue-slide .slide-wrap {
    display: flex;
    width: max-content;
  }
</style>
<template>
   <div class="mpvue-slide">
     <div
      class="slide-wrap"
      @touchstart="touchstart"
      @touchmove="touchmove"
      :animation="animationData">
      <slot></slot>
     </div>
   </div>
</template>
<script>
  import { boundingClientRect, slideAnimate } from './utils/adapter'
  export default {
    props: {
      speed: {
        type: Number,
        default: 17
      },
      isStick: {
        type: Boolean,
        default: false
      }
    },
    data () {
      return {
        animationData: {
          transformOrigin: '50% 50%',
          duration: 300,
          timingFunction: 'ease',
          delay: 0
        },
        startX: 0,
        transX: 0,
        wrapWidth: 0,
        slideWidth: 0
      }
    },
    computed: {
      transBoundary () {
        return [- (this.wrapWidth - this.slideWidth), 0]
      }
    },
    methods: {
      /**
       * @description 设置startX， wrapWidth， slideWidth
       */
      async touchstart (e) {
        // 获取startX 在mpvue中会有mp属性
        if (e.mp !== undefined) {
          this.startX = e.mp.touches[0].clientX
        } else {
          this.startX = e.touches[0].clientX
        }

        // 获取wrap层的宽度
        const $wrapRect = await boundingClientRect('.mpvue-slide > .slide-wrap')
        this.wrapWidth = $wrapRect.width
        this.wrapWidth = 460

        const $slideRect = await boundingClientRect('.mpvue-slide')
        this.slideWidth = $slideRect.width
      },
      touchmove (e) {
        // 获取distance
        let moveX = 0
        if (e.mp !== undefined) {
          moveX = e.mp.touches[0].clientX
        } else {
          moveX = e.touches[0].clientX
        }

        const distance = moveX - this.startX
        this.startX = moveX
        this.transX = this.transX + distance
        // 边界检测
        this.transX = this.getSafeValue(this.transX, this.transBoundary)
        // 创建动画 动画移动跟随distance
        this.animationData = slideAnimate(this.speed, this.transX, '.mpvue-slide>.slide-wrap')
      },
      /**
       * @desc 获取偏移的安全距离
       * @param {number} transX - 横向偏移量
       * @param {Array} boundary 偏移范围 例如[-100, 0]
       * @return {number} 获取偏移的安全距离
       */
      getSafeValue (transX, boundary) {
        if (transX > boundary[1]) {
          return boundary[1]
        }
        if (transX < boundary[0]) {
          return boundary[0]
        }
        return transX
      }
    }
  }
</script>
