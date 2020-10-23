<template>
	<view class="home-categories-container">
		<uni-grid :column="4" :showBorder="false">
			<uni-grid-item class="home-category-item">
				<view class="home-category-item-icon">
					<image class="home-category-item-image" src="../../static/image/home/kitchen.png"></image>
				</view>
				<view class="home-category-item-name">
					<text class="text">餐具</text>
				</view>
			</uni-grid-item>
			<uni-grid-item class="home-category-item">
				<view class="home-category-item-icon">
					<image class="home-category-item-image" src="../../static/image/home/bottle.png"></image>
				</view>
				<view class="home-category-item-name">
					<text class="text">杯具</text>
				</view>
			</uni-grid-item>
			<uni-grid-item class="home-category-item">
				<view class="home-category-item-icon">
					<image class="home-category-item-image" src="../../static/image/home/foods.png" mode=""></image>
				</view>
				<view class="home-category-item-name">
					<text class="text">美食</text>
				</view>
			</uni-grid-item>
			<uni-grid-item class="home-category-item">
				<view class="home-category-item-icon">
					<image class="home-category-item-image" src="../../static/image/home/dailyuse.png"></image>
				</view>
				<view class="home-category-item-name">
					<text class="text">日用</text>
				</view>
			</uni-grid-item>
		</uni-grid>
	</view>
</template>

<script>
	import uniGrid from "@/components/uni-grid/uni-grid.vue"
	import uniGridItem from "@/components/uni-grid-item/uni-grid-item.vue"
	export default {
		components: {
			uniGrid,
			uniGridItem
		}
	}
</script>

<style lang="scss">
	.home-categories-container {
		padding: $uni-spacing-row-base;

		.home-category-item {
			display: flex;
			align-items: center;
			justify-content: center;

			.home-category-item-icon {
				text-align: center;

				.home-category-item-image {
					width: 100rpx;
					height: 100rpx;
					border-radius: $uni-border-radius-base;
					background: $uni-bg-color-grey;
				}
			}

			.home-category-item-name {
				text-align: center;
				color: $uni-color-primary;
			}
		}
	}
</style>
