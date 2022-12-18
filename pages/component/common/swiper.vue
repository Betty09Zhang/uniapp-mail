<template>
	<view>
		<swiper class="swiper" circular :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval"
				:duration="duration">
				<swiper-item v-for="(img, index) in imagesArr" :key="index">
					<view>
						<image :src="img" style="height: 350upx;width: 100%;" @tap="clickImage"></image>
					</view>
				</swiper-item>
		</swiper>
	</view>
	
</template>

<script>
	export default {
		props: {
			imagesArr: {
				type: Array
			}
		},
		methods: {
			clickImage(event) {
				console.log(`click...`)
			}
		},
		data() {
			return {
				background: ['color1', 'color2', 'color3'],
				indicatorDots: true,
				autoplay: true,
				interval: 2000,
				duration: 500
			}
		}
	}
</script>

<style>
</style>