<template>
	<view>
		<view class="flex align-center">
			<view class="flex align-center justify-center" style="width: 180rpx;height: 180rpx;">
				<image src="/static/gift/4.png" class="rounded-circle" style="width: 105rpx;height: 105rpx;"></image>
			</view>
			<view class="flex flex-column">
				<text class="font-md">昵称</text>
				<text class="font text-muted">描述</text>
			</view>
			<view class="ml-auto mr-3">
				<view class="p-2 border border-main rounded flex align-center justify-center" hover-class="bg-light">
					<text class="font text-main">编辑资料</text>
				</view>
			</view>
		</view>
		<view class="f-divider"></view>
		<view class="p-3 flex align-center" hover-class="bg-light">
			<text class="iconfont iconliwu mr-3"></text>
			<text class="font-md">我的金币</text>
			<text class="ml-auto">
				<text class="text-muted font">
					50金币 立即充值
				</text>
			</text>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
		methods: {

		}
	}
</script>

<style>

</style>
