<template>
<view class="container">
  <video-cover />
  <SpotDesc />
  <line-list /> 
</view>
</template>

<script>
import VideoCover from '@/components/VideoCover/index.vue'
import SpotDesc from '@/components/SpotDesc/index.vue'
import LineList from '@/components/LineList/index.vue'


export default {
  data() {
    return {}
  },
  components: {
    VideoCover,
    SpotDesc,
    LineList
  }
}
</script>

<style>
.container {
  height: 100%;
  text-align: center;
  display: block;
  align-items: center;
  justify-content: center;
}
</style>
