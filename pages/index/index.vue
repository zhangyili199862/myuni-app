<template>
	<view>
		<!-- 轮播图  -->
		<swiper class="swiper" :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000"
			style="width: 750rpx;height: 250rpx;">
			<swiper-item>
				<image src="../../static/demo/banner/1.jpg" style="width: 100%;height: 100%;"></image>
			</swiper-item>
			<swiper-item>
				<image src="../../static/demo/banner/2.jpg" style="width: 100%;height: 100%;"></image>
			</swiper-item>
		</swiper>
		<view class="flex flex-wrap">
			<view class="list-box" v-for="i in 10" :key="i" @click="openLive">
				<image class="rounded" src="../../static/demo/1.jpg" style="width: 365rpx;height: 365rpx;"
					mode="aspectFill"></image>
				<view class="rounded-circle absolute-left-top">
					<text class="iconfont iconbizhongguanli text-warning">
						<text class="text-white font">0</text>
					</text>
				</view>
				<view class="rounded-circle absolute-right-top">
					<text class="text-white font-sm">人气:</text><text class="text-white font">0</text>
				</view>
				<view class="rounded-circle absolute-left-bottom">
					<text class="text-white font-sm">标题</text>
				</view>
				<view class="rounded-circle absolute-right-bottom">
					<text class="rounded-circle bg-danger color-point"></text><text
						class="text-white font-sm">已结束</text>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {}
		},
		onLoad() {

		},
		methods: {
		openLive(){
			uni.navigateTo({
				url:'../live/live'
			})
		}
		}
	}
</script>

<style>
	.list-box {
		position: relative;
		width: 365rpx;
		height: 365rpx;
		margin: 5rpx;
	}

	.absolute-left-top {
		display: flex;
		align-items: center;
		position: absolute;
		top: 15rpx;
		left: 15rpx;
		background-color: rgba(0, 0, 0, 0.4);
		padding: 10rpx 20rpx;
	}

	.absolute-right-top {
		display: flex;
		align-items: center;
		position: absolute;
		top: 15rpx;
		right: 15rpx;
		background-color: rgba(0, 0, 0, 0.4);
		padding: 0 20rpx;
	}

	.absolute-left-bottom {
		display: flex;
		align-items: center;
		position: absolute;
		left: 15rpx;
		bottom: 15rpx;
	}

	.absolute-right-bottom {
		display: flex;
		align-items: center;
		position: absolute;
		right: 15rpx;
		bottom: 15rpx;
		background-color: rgba(0, 0, 0, 0.4);
	}

	.color-point {
		width: 20rpx;
		height: 20rpx;
		margin-right: 10rpx;
	}
</style>
