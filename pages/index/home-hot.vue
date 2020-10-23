<template>
	<view class="home-hot-container">
		<swiper class="hot-swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration" :circular="circular">
			<swiper-item v-for="item in data" :key="item.id">
				<view class="hot-swiper-item">
					<a href="javascript:;" @click="$emit('jump-detail',item)">
						<img :src="item.url" :alt="item.title">
					</a>
				</view>
			</swiper-item>
		</swiper>
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
				indicatorDots: true,
				autoplay: true,
				circular: true,
				interval: 2000,
				duration: 500
			}
		}
	}
</script>

<style lang="scss">
	.hot-swiper{
		.hot-swiper-item {
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
