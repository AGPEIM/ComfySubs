<template>
	<div id="wrapper">
		<img id="logo" src="~@/assets/main.png" alt="electron-vue">
		<div class="c_1">轻点一下，轻松字幕</div>
		<div class="c_2">欢迎使用ComfySubs</div>
		<div class="btn">
			<button type="success">打开视频</button>
		</div>
		
	</div>
</template>

<script>
	import SystemInformation from './LandingPage/SystemInformation'

	export default {
		name: 'landing-page',
		components: {
			SystemInformation
		},
		methods: {
			open(link) {
				this.$electron.shell.openExternal(link)
			}
		}
	}
</script>

<style>
	@import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');

	* {
		box-sizing: border-box;
		margin: 0;
		padding: 0;
	}

	#logo {
		height: auto;
		margin-bottom: 20px;
		margin-left: 55px;
		margin-top: 20px;
		width: 280px;
	}

	.c_1 {
		font-size: 32px;
		font-family: "PingFang SC";
		font-weight: 500;
		color: #282828;
		text-align: center;
	}

	.c_2 {
		margin-top: 5px;
		font-size: 16px;
		font-family: "PingFang SC";
		font-weight: 400;
		color: #888b8b;
		text-align: center;
	}
	.btn button{
		width: 230px;
		height: 60px;
		position: relative;
		left: 80px;
		top: 50px;
		font-size: 22px;
		font-weight: 600;
		color: white;
		border: none;
		background-color: #0FCF94;
	}
</style>
