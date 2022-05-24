<template>
	<view class="content">
        <view class="line">
            <text @click="goto('/pages/plugin/plugin')">测试：本地原生插件 DCloud-RichAlert</text>
        </view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello 2022 5051'
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

    .line {
        display: flex;
        flex-direction: column;
        position: relative;
        background-color: antiquewhite;
        width: 100%;
        margin-top: 10rpx;
    }
	.line > text{
        padding: 10rpx 30rpx;
        height: 80rpx;
        line-height: 80rpx;
        font-size: 30rpx;
    }
</style>
