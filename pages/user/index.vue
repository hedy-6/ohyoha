<template>
	<view class="container">
		我叫{{userInfo.name}}
	</view>
</template>

<script>
	export default {
		data() {
			return {
				userInfo: {
					name: "小王"
				}
			}
		},
		methods: {
	
		}
	}
</script>

<style>
</style>
