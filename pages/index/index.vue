<template>
	<view class="content">
        <view class="line">
            <text @click="goto('/pages/plugin/plugin')">测试：本地原生插件 DCloud-RichAlert</text>
        </view>

        <view class="line">
            <text @click="goto('/pages/plugin-cloud/plugin-cloud', 'Android')">测试：云端原生插件 Aq-ChooseFile</text>
        </view>
        <view class="line">
             <text @click="goto('/pages/test/test')">测试：日志打印</text>
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
			goto(url, platform="all") {

                // #ifdef APP-PLUS
                let osName;
                osName = plus.os.name;
                if (osName != platform && platform != 'all') {
                    uni.showModal({
                        title: "此功能仅适用于" + platform,
                        showCancel: false,
                        confirmText: '我知道了'
                    });
                    return;
                };
                // #endif

				uni.navigateTo({
					url: url
				});
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
