<template>
		<!-- <image class="logo animate animate__bounceIn animate__fast" src="/static/logo.png" v-if="show"></image>
		<view class="text-area">
			<text class="title" @tap="show=!show">{{title}}</text>
		</view>
		<view class="icon-31xiaoxi iconfont"></view> -->
		<!-- <swiper class="swiper" circular :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval"
				:duration="duration">
				<swiper-item v-for="(img, index) in imagesArr" :key="index">
					<view>
						<image :src="img" style="height: 350upx;width: 100%;" @tap="clickImage"></image>
					</view>
				</swiper-item>
		</swiper> -->
	<view>
		<swiper-component :imagesArr="imagesArr"></swiper-component>	
		<view>
			<view class="row fx-wrap justify-center align-center pd-20">
				<view class="item justify-center align-center" v-for="itemObj in listArr">
					<image :src="itemObj.image" style="width:60upx;height: 60upx;"></image>
					<text class="text">{{itemObj.name}}</text>
				</view>
			</view>
		</view>
	</view>
		
	
</template>

<script>
	import SwiperComponent from '../component/common/swiper.vue'
	export default {
		components: {
			SwiperComponent
		},
		data() {
			return {
				title: 'Hello',
				show: false,
				background: ['color1', 'color2', 'color3'],
				indicatorDots: true,
				autoplay: true,
				interval: 2000,
				duration: 500,
				imagesArr: ['../../static/images/demo/demo4.jpg',
				'../../static/images/demo/demo4.jpg',
				'../../static/images/demo/demo4.jpg',
				],
				listArr: [{image: '../../static/images/indexnav/1.png', name: '新品发布'},
				{image: '../../static/images/indexnav/2.gif', name: '小米众筹'},
				{image: '../../static/images/indexnav/3.gif', name: '以旧换新'},
				{image: '../../static/images/indexnav/4.gif', name: '一分换团'},
				{image: '../../static/images/indexnav/5.gif', name: '超值特卖'},
				{image: '../../static/images/indexnav/6.gif', name: '小米秒杀'},
				{image: '../../static/images/indexnav/7.gif', name: '真心想要'},
				{image: '../../static/images/indexnav/8.gif', name: '电视热卖'},
				{image: '../../static/images/indexnav/9.gif', name: '家电热卖'},
				{image: '../../static/images/indexnav/10.gif', name: '米粉卡'}]
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
	.list {
		height: 288rpx;
		background-color: yellow;
		flex-wrap: wrap;
		display: flex;
		flex-direction: row;
		box-sizing: border-box;
		justify-content: center;
		align-items: center;
	}
	.item {
		width: 20%;
		background-color: #8f8f94;
		/* height: 50%;
		text-align: center; */
		
		display: flex;
		flex-direction: column;
	}
</style>
