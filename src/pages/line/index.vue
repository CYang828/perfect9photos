<template>
<view class="container">
  <map-cover />
  <line-desc />
</view>
</template>

<script>
import MapCover from '@/components/MapCover/index.vue'
import LineDesc from '@/components/LineDesc/index.vue'


export default {
  components: {
    MapCover,
    LineDesc
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
