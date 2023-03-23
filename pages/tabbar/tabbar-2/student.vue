<template>
	<view class="content">
		<view>
			<scroll-view class="scroll-view_H" scroll-x="true" scroll-left="0">
				<image class="scroll-view-item_H" src="/static/img/school//abds.png"></image>
				<image class="scroll-view-item_H" src="/static/img/school/ghn.png"></image>
				<image class="scroll-view-item_H" src="/static/img/school/sanyi.png"></image>
				<image class="scroll-view-item_H" src="/static/img/school/qn.png"></image>
			</scroll-view>

			<uni-grid class="gridview" :column="4" :show-border="false" @change="onGridItemClick">
				<uni-grid-item v-for="(item, index) in ghnList" :index="index">
					<view class="griditem">

						<image class="header" src="/static/img/school/qn.png"></image>

						<view><span>{{item.name}}</span></view>
					</view>
				</uni-grid-item>
			</uni-grid>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				items: [{
						message: 'Foo'
					},
					{
						message: 'Foo'
					},
					{
						message: 'Foo'
					},
					{
						message: 'Foo'
					},
					{
						message: 'Foo'
					},
					{
						message: 'Foo'
					},

					{
						message: 'Bar'
					}
				],
				abdsList: [{
						name: "陆八魔亚瑠",
						age: "16",
						sg: "160cm"
					},

				],
				ghnList: [{
						name: "陆亚瑠",
						age: "16",
						sg: "160cm",
						info: "",
						cost: "4",
						skillex: "",
						skill1: "",
						skill2: "",
						skill3: "",
						skillimgex: "",
						skillimg1: "",
						skillimg2: "",
						skillimg3: "",
						updateNeed: "",
						updateNeedImg1: "",
						updateNeedImg2: "",
						showVideo: "",
						datingImg: ""
					},
					{
						name: "陆八魔亚瑠",
						age: "16",
						sg: "160cm",
						info: "",
						cost: "4",
						skillex: "",
						skill1: "",
						skill2: "",
						skill3: "",
						skillimgex: "",
						skillimg1: "",
						skillimg2: "",
						skillimg3: "",
						updateNeed: "",
						updateNeedImg1: "",
						updateNeedImg2: "",
						showVideo: "",
						datingImg: ""
					}
				]
			}
		},
		onLoad() {

		},
		methods: {
			onGridItemClick(e) {
				//在起始页面跳转到test.vue页面并传递参数
				uni.navigateTo({
					url: '/pages/detial/studentDetial/studentDetial?id=1&name=uniapp'
				});
				console.log(e.detail.index)
			}
		}
	}
</script>

<style lang="scss">
	.content {
		text-align: center;
	}

	.scroll-view_H {
		white-space: nowrap;
		width: 100%;
	}

	.scroll-view-item_H {
		width: 200rpx;
		height: 150rpx;
		margin-left: 20rpx;
	}

	.gridview {
		background-color: gray;
		margin-top: 30rpx;
	}

	.griditem {
		width: 100%;
		height: 100%;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	.header {
		width: 90%;
		height: 90%;
	}

	.grid {
		justify-content: center;
	}
</style>
