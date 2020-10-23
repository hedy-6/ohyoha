<template>
	<view class="home-recommend-container">
		<view v-for="item in data" :key="item.id">
			<view class="recommend-item">
				<a href="javascript:;" @click="$emit('jump-detail',item)">
					<img :src="item.url" :alt="item.name">
				</a>
			</view>
		</view>
		<uni-list>
		    <uni-list-item v-for="item in data" :key="item.id" :title="item.name" :note="item.desc">
		        <template v-slot:header>
		            <view class="uni-thumb"><image :src="item.url" mode="aspectFill"></image></view>
		        </template>
		    </uni-list-item>
		</uni-list>
	</view>
</template>

<script>
	export default {
		props: {
			data: {
				type: Array,
				default: () => []
			}
		},
		data() {
			return {
			}
		}
	}
</script>

<style lang="scss">
	.home-recommend-container {
		.recommend-item {
			margin-bottom: $uni-spacing-row-base;
			&>a {
				display: block;

				img {
					width: 100%;
					height: 100%;
				}
			}
		}
	}
</style>
