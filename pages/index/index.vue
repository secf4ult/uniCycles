<template>
  <view class="container">
    <view class="intro">
      <map :latitude="lat" :longitude="lon" :markers="markers"></map>
    </view>
  </view>
</template>

<script>
export default {
	data() {
		return {
			lat: '',
       lon: '',
       covers: [
       // format
       // {
       //   latitude: 0,
       //   longitude: 0,
       //   iconPath: ''
       // },
       ]
		}
	},
   onLoad() {
     plus.geolocation.getCurrentPosition((p) => {
       { latitude: lat, longitude: lon} = p.coords
     })
   },
	methods: {

	}
}
</script>

<style>
.container {
  padding: 20px;
  font-size: 14px;
  line-height: 24px;
}
</style>
