<template>
	<scroll-view scroll-y="true" style="width: 520rpx;height: 300rpx;" scroll-with-animation class="pl-3"
		:scroll-into-view="scrollInToView" >
		<view :id="'danmu'+item.id"  class="flex justify-start align-start rounded p-2 mb-2"
			style="background-color: rgba(255,255,255,0.125);" v-for="(item,index) in list" :key="index">
			<text class="font-md text-danger">{{item.userName}}:</text>
			<text class="font-md text-white">{{item.content}}</text>
		</view>

	</scroll-view>
</template>

<script>
	export default {
		data() {
			return {
				list: [],
				scrollInToView:""
			}
		},
		methods: {
			toBottom() {
				setTimeout(() => {
					let len = this.list.length;
					if (len > 0 && this.list[len - 1]) {
						this.scrollInToView = 'danmu' + this.list[len - 1].id
					}
				}, 200)
			},
			send(danmu){
				this.list.push(danmu)
				this.toBottom();
			}
		},
		mounted() {
		}
	}
</script>

<style>

</style>
