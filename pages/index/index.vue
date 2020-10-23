<template>
	<view class="container home-cotainer">
		<view class="home-search">
			<uni-search-bar @confirm="search"></uni-search-bar>
		</view>
		<!-- 热门推荐商品 -->
		<view class="home-hot">
			<home-hot :data="hotData" @jump-detail="onJumpDetail" />
		</view>
		<!-- 分类标签 -->
		<view class="home-categories">
			<home-category />
		</view>
		<!-- 分割线 -->
		<view class="home-divider">
			<label class="home-divider-left" for="">——</label>
			<text>热门推荐</text>
			<label class="right" for="">——</label>
		</view>
		<!-- 相关推荐 -->
		<view class="home-recommend">
		<home-recommend :data="recommendData"  @jump-detail="onJumpDetail"/>
		</view>

		<view class="intro">本项目已包含uni ui组件，无需import和注册，可直接使用。在代码区键入字母u，即可通过代码助手列出所有可用组件。光标置于组件名称处按F1，即可查看组件文档。</view>
		<text class="intro">详见：</text>
		<uni-link :href="href" :text="href"></uni-link>
	</view>
</template>

<script>
	import uniSearchBar from '@/components/uni-search-bar/uni-search-bar.vue'
	import homeHot from './home-hot.vue'
	import homeCategory from './home-category.vue'
	import homeRecommend from './home-recommend.vue'
	import {
		hotData,
		recommendData
	} from './datas.js'
	
	export default {
		components: {
			uniSearchBar,
			homeHot,
			homeCategory,
			homeRecommend
		},
		data() {
			return {
				href: 'https://uniapp.dcloud.io/component/README?id=uniui',
				hotData,
				recommendData,
			}
		},
		methods: {
			// 搜索
			search({
				value
			}) {
				console.info('value', value)
			},
			// 跳转到商品详情
			onJumpDetail({
				id
			}) {
				uni.navigateTo({
					url: `/pages/good/index?id=${id}`
				});
			}
		}
	}
</script>

<style lang="scss">
	.home-cotainer {
		min-height: calc(100vh - 94px);
		background: $uni-bg-color-grey;

		.home-categories {
			background: #fff;
		}

		.home-divider {
			margin: $uni-spacing-row-base 0;
			text-align: center;
			color: $uni-text-color-grey;

			label {
				margin: 0 20rpx;
			}
		}
	}
</style>
