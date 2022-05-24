<template>
	<view class="content">
        <uni-list>
            <uni-list-item @click="goto('/pages/plugin/plugin')" >测试：原生插件</uni-list-item>
        </uni-list>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello 2022'
			}
		},
		onLoad() {

		},
		methods: {
			goto(url) {
				uni.navigateTo({
					url: url
				})
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

	uni-list > uni-list-item {
        height: 100rpx;
        width: 100%;
        line-height: 100rpx;
        display: block;
        text-align: start;
        border-bottom: 1px solid #000;
    }
</style>
