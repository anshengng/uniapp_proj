<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"> </image>
		<view class="text-area">
			<text class="title">{{ title }}</text>
		</view>
		<up-button type="primary" text="确定"  @click="clickHan"></up-button>
	</view>
</template>

<script setup>
import { ref } from "vue";
const title = ref("www");

const clickHan = () => {
	uni.navigateTo({
		url: "/subpkg_task/detail/detail",
	});
};
</script>

<style>
.content {
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
}

.logo {
	height: 200rpx;
	width: 200rpx;
	margin-top: 200rpx;
	margin-left: auto;
	margin-right: auto;
	margin-bottom: 50rpx;
}

.text-area {
	display: flex;
	justify-content: center;
}

.title {
	font-size: 36rpx;
	color: #8f8f94;
}
</style>
