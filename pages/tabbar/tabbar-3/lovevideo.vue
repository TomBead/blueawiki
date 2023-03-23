<template>
	<view class="content">
		<scroll-view :scroll-top="scrollTop" scroll-y="true" class="scroll-Y" @scrolltoupper="upper"
			@scrolltolower="lower" @scroll="scroll">
			<view>
				<view class="activity">
					<video :src="videourl"></video>
				</view>
				
				
				
			</view>
		</scroll-view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				videourl: "https://njc-download.weiyun.com/ftn_handler/da91791eeb08b7faa33f15791cc08463c487725ee3078e561ad02975da9dae36/10000_Title_Video_tw.mp4?fname=10000_Title_Video_tw.mp4&from=30013&version=3.3.3.3",
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
		text-align: center;
		height: 400upx;
	}
	.activity{
		width: 100%;
		margin-top: 50rpx;
	}
</style>
