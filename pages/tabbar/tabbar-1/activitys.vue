<template>
	<view class="content">
		<scroll-view :scroll-top="scrollTop" scroll-y="true" class="scroll-Y" @scrolltoupper="upper"
			@scrolltolower="lower" @scroll="scroll">
			<view>
				<view class="activity">
					<h3>{{activity.title}}</h3>
					<view><span>{{activity.time}}</span></view>
					<image :src="activity.imgurl">
					</image>
				</view>

				<view class="activity">
					<h3>抽取UP</h3>
					<view><span>{{upStudent.time}}</span></view>

					<view v-for="(item,index) in upStudent.studentList" :key="index">
						<image class="zlzimg" :src="item.imgurl">
						</image>
						<view><span> {{item.name}}</span></view>
					</view>
				</view>

				<!-- 总力战 -->
				<view class="activity">
					<h3>总力战</h3>
					<view><span>{{zlz.time}}</span></view>
					<image class="zlzimg" :src="zlz.imgurl"></image>
					<view><span>{{zlz.name}}</span></view>
				</view>
				<!-- 总力战end -->
				<!--  -->
				<view class="activity">
					<h3>综合战术考试</h3>
					<view><span>{{zhTest.time}}</span></view>
					<image class="zlzimg" :src="zhTest.imgurl"></image>
					<view><span>{{zhTest.name}}</span></view>
				</view>
			</view>
		</scroll-view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				activity: {
					title: "风纪委员会的地狱夏季合宿训练",
					time: "2023.3.14 10:00~2023.3.20 9:59",
					imgurl: "https://jarvis.dn.nexoncdn.co.kr/bluearchive/gb/20230314/20230314074458634-080741b4a78c44a3900eb53b6b17b1f6.png"
				},
				upStudent: {
					time: "2023.3.14 10:00~2023.3.20 9:59",
					studentList: [{
							name: '3★八神(泳裝)',
							imgurl: "https://d30y0swoxkbnsm.cloudfront.net/forum/20230313/6bc97343-dfbb-4e8d-a07d-fa5222890cfe/BA_%ED%94%BD%EC%97%85-%ED%9E%88%EB%82%98(Twitter).jpg",
						},
						{
							name: '3★陽奈(泳裝)',
							imgurl: "https://d30y0swoxkbnsm.cloudfront.net/forum/20230313/6bc97343-dfbb-4e8d-a07d-fa5222890cfe/BA_%ED%94%BD%EC%97%85-%ED%9E%88%EB%82%98(Twitter).jpg",
						},
						{
							name: '3★陽奈(泳裝)',
							imgurl: "https://d30y0swoxkbnsm.cloudfront.net/forum/20230313/6bc97343-dfbb-4e8d-a07d-fa5222890cfe/BA_%ED%94%BD%EC%97%85-%ED%9E%88%EB%82%98(Twitter).jpg",
						},
					],
				},

				zlz: {
					time: "2023.3.14 10:00~2023.3.20 9:59",
					name: "全面进攻 - 希罗尼穆斯（城市战）",
					imgurl: "https://jarvis.dn.nexoncdn.co.kr/bluearchive/gb/20230314/20230314074458634-080741b4a78c44a3900eb53b6b17b1f6.png"

				},
				zhTest: {
					time: "2023.3.14 10:00~2023.3.20 9:59",
					name: "奈落",
					imgurl: "https://jarvis.dn.nexoncdn.co.kr/bluearchive/gb/20230314/20230314074458634-080741b4a78c44a3900eb53b6b17b1f6.png"

				}
			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.activity {
		width: 100%;
		text-align: center;
		margin-top: 50rpx;
	}

	.zlzimg {
		height: 380rpx;
		background-color: aquamarine;
		width: 100%;
	}
</style>
