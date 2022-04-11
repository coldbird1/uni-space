<template>
	<view class="content">
		<image class="logo" src="/static/logo.png" @click="imgFn()"></image>
		<view class="text-area">
			<text class="title">{{title}}</text>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {
          imgFn(){
			uni.navigateTo({
				url: '/pages/index/detail',
				success: res => {},
				fail: () => {},
				complete: () => {}
			});
			// uni.navigateTo({
			// 	url: '/pages/comment/add?image=' + image,
			// 	success: res => {},
			// 	fail: () => {},
			// 	complete: () => {}
			// });
		  }
			
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
</style>
